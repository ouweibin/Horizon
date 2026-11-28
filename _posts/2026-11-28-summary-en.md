---
layout: default
title: "Horizon Summary: 2026-11-28 (EN)"
date: 2026-11-28
lang: en
---

> From 28 items, 7 important content pieces were selected

---

1. [OpenSec Discloses CVSS 9.8 Pre-Auth Root Flaw in Linux NFS Server](#item-1) ⭐️ 9.0/10
2. [Google's Depth-wise Cross-Attention rewires transformer residual connections for up to 3x speedups](#item-2) ⭐️ 8.0/10
3. [WebRTC-based credit card skimmers found on popular shopping sites](#item-3) ⭐️ 8.0/10
4. [Convex AI coding skill accused of silently uploading user app ideas](#item-4) ⭐️ 8.0/10
5. [State attorneys general sue SpaceX over Grok's generation of abuse imagery](#item-5) ⭐️ 8.0/10
6. [SemiAnalysis: Trainium3 Inference Beats GB300 on Performance TCO](#item-6) ⭐️ 8.0/10
7. [Minecraft Java Edition Hit by Minecraft2Shell RCE via Crafted Resource-Pack Fonts](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenSec Discloses CVSS 9.8 Pre-Auth Root Flaw in Linux NFS Server](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 9.0/10

OpenSec has published details of CVE-2026-99362, a CVSS 9.8 pre-authentication heap overflow in the Linux kernel's NFS server daemon (nfsd) that lets an unauthenticated attacker write 61 bytes past a kernel heap object via a single connection to tcp/2049 and, by chaining that primitive, obtain a root shell. The flaw has existed since Linux 3.16 (2014) and affects any host serving NFSv4.1 or 4.2, with fixes already released in kernels 6.12.117, 6.18.61, 7.3.2 and 7.4-rc1. NFS is one of the most widely deployed network file systems in enterprise and home environments, so this flaw potentially exposes file servers, NAS appliances and cluster storage nodes to unauthenticated remote takeover with no user interaction required. Because the vulnerable code lives in the kernel and predates 2014, an enormous installed base of long-term-support distributions and embedded storage devices will need kernel upgrades and reboots, making this an urgent patching priority. Exploitation requires that NFSv4.1 or 4.2 be served on a reachable tcp/2049, and the overflow itself only writes 61 bytes past a kernel heap object, so a working root exploit depends on heap grooming and chaining rather than a single-shot primitive. The advisory notes that administrators who cannot reboot immediately should restrict access to tcp/2049 at the firewall as a mitigation; the CVE was made public on November 20, 2026.

telegram · zaihuapd · Nov 27, 12:57

**Background**: NFS (Network File System) is a protocol that lets a machine mount and use directories hosted on another machine over the network, and on Linux the server side is implemented largely inside the kernel by the nfsd component rather than as a pure userspace daemon. NFSv4.1 and 4.2 are modern revisions of the protocol that add features such as session trunking and server-side copy, and they listen on TCP port 2049. A heap overflow is a memory-safety bug where more data is written than a heap-allocated buffer can hold, corrupting adjacent kernel structures; a 'pre-auth' bug means the corruption happens during connection or protocol handling, before any credential check, so no account or password is needed.

<details><summary>References</summary>
<ul>
<li><a href="https://opensec.in/blog/nfs2root-cve-2026-99362">NFS2ROOT (CVE-2026-99362): pre - auth root in Linux nfsd | OpenSec</a></li>
<li><a href="https://wiki.archlinux.org/title/NFS">NFS - ArchWiki</a></li>

</ul>
</details>

**Tags**: `#Linux kernel`, `#NFS`, `#security vulnerability`, `#CVE`, `#remote privilege escalation`

---

<a id="item-2"></a>
## [Google's Depth-wise Cross-Attention rewires transformer residual connections for up to 3x speedups](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 8.0/10

Google Research published a blog post introducing Depth-wise Cross-Attention (DCA), a redesign of transformer residual connections in which each token attends over the embeddings of all prior layers rather than simply adding the previous layer's output. In their experiments, DCA reportedly delivers comparable model quality while training and running inference up to 3x faster, i.e., a better quality-per-FLOP tradeoff. Residual (skip) connections have been essentially unchanged since the original 2017 transformer, so a cheaper alternative to stacking depth touches everyone who trains or serves large language models. If the 3x quality-per-FLOP gain holds at scale, it directly lowers training compute cost and inference latency and could make models like Gemini cheaper and faster to run. DCA splits queries, keys and values so that attention is applied across depth (layers) instead of only across the token sequence, with each token querying a dynamically weighted mix of all prior layer embeddings, avoiding the quadratic cost of scaling attention over a longer token sequence. The claims come from Google's own benchmarks on language modeling, so independent reproduction and behavior at frontier scale remain open questions.

hackernews · ComputedCamp995 · Nov 27, 23:06 · [Discussion](https://news.ycombinator.com/item?id=50672565)

**Background**: A transformer is a stack of identical blocks, each containing an attention sub-layer that mixes information across tokens in a sequence and a feed-forward sub-layer that processes each token. Residual connections, introduced with ResNet in 2015, add a block's input back to its output so gradients can flow through dozens or hundreds of layers without vanishing; in standard transformers each block only sees the output of the immediately preceding block. FLOPs (floating-point operations) are the hardware-independent way researchers measure computational cost, so "quality per FLOP" compares architectures by how much model quality they buy for a fixed amount of compute. DCA changes the skip connection from a plain addition into a learned attention over the whole history of layer embeddings.

<details><summary>References</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections</a></li>
<li><a href="https://poloclub.github.io/transformer-explainer/">Transformer Explainer: LLM Transformer Model Visually Explained</a></li>
<li><a href="https://blog.authon.dev/standard-transformer-attention-vs-attention-residuals-a-practical-comparison">Standard Transformer Attention vs. Attention- Residuals ... | Authon Blog</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were largely positive: one user said Gemini "Neon" feels insanely cheap and fast relative to Claude Opus and wondered whether DCA explains it, while another mused that attention over all prior layers might finally address the infamous "strawberry" counting/reasoning failure. Others drew parallels to DenseNet's dense connectivity and made a minor complaint that the result charts should be bar charts rather than line graphs.

**Tags**: `#transformers`, `#llm-architecture`, `#google-research`, `#attention-mechanisms`, `#training-efficiency`

---

<a id="item-3"></a>
## [WebRTC-based credit card skimmers found on popular shopping sites](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 8.0/10

Researchers discovered credit card skimming scripts that abuse WebRTC on popular shopping sites, with the campaign reportedly timed around Black Friday; the scripts target mobile users and use WebRTC to evade detection. The finding highlights how third-party scripts on e-commerce sites remain a major supply-chain risk, and it shows that attackers can bypass common monitoring by using less-inspected browser APIs during peak holiday shopping. WebRTC itself is a legitimate real-time communication API, so the issue is not a WebRTC vulnerability but the fact that its data channels are rarely inspected; commenters noted the same exfiltration could be done with ordinary HTTP requests, and the mobile focus makes detection harder. The provided summary did not name the affected retailers or give a count of compromised sites.

hackernews · scanr · Nov 27, 15:40 · [Discussion](https://news.ycombinator.com/item?id=50668145)

**Background**: WebRTC (Web Real-Time Communication) is an open-source browser API for peer-to-peer audio, video and data communication, standardized by the W3C and IETF and supported by Apple, Google, Microsoft, Mozilla and Opera. Credit card skimming scripts, often called Magecart scripts, are JavaScript injected into online stores to harvest payment card data as customers enter it. Many e-commerce sites load dozens of third-party scripts for analytics, advertising and chat widgets, which greatly expands the attack surface.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebRTC">WebRTC</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-abuse-google-apps-script-to-steal-credit-cards-bypass-csp/">Hackers abuse Google Apps Script to steal credit cards , bypass CSP</a></li>
<li><a href="https://www.zdnet.com/article/inter-a-low-bar-kit-for-magecart-website-credit-card-skimmer-attacks/">Inter: a ‘low bar’ kit for Magecart credit card skimmer attacks... - ZDNET</a></li>

</ul>
</details>

**Discussion**: Commenters argued the incident justifies ad and script blocking, while several noted WebRTC is not technically special—its channels are simply less monitored, and plain HTTP could achieve the same theft. Others criticized the web's model of running third-party code in the browser and questioned why ad networks and browsers do not sandbox ads or disable JavaScript execution for them.

**Tags**: `#security`, `#web-security`, `#e-commerce`, `#skimming`, `#WebRTC`

---

<a id="item-4"></a>
## [Convex AI coding skill accused of silently uploading user app ideas](https://github.com/convex/convex-backend-skill/issues/64) ⭐️ 8.0/10

A GitHub issue (convex/convex-backend-skill#64) alleges that Convex's AI coding skill silently sends users' app ideas and prompts to a remote server without telling them. The report reached the front page of Hacker News with roughly 269 points and 87 comments, and Convex CEO Jamie responded in the thread to clarify what the upload is for. AI coding "skills" are plain-instruction packages that agents such as Claude Code, Cursor and Codex load and follow automatically, so a hidden network call inside one touches both user privacy and trust in the whole skill-distribution ecosystem. Because Convex also stores customers' data and code and runs an AI gateway, the dispute raises the broader question of how much a vendor in the AI tooling path should be trusted by default. In the thread, CEO Jamie explained that the prompt upload powers Convex's "quickstart" feature, which he described as the spiritual successor to Convex Chef, an end-to-end "vibe-coding" product that Convex recently shut down. Commenters noted that the dispute blurs two distinct risks: deliberate data collection versus prompt injection, which several said is far more common than a model making malicious tool calls on its own.

hackernews · MickyTheMouse · Nov 27, 18:02 · [Discussion](https://news.ycombinator.com/item?id=50669765)

**Background**: Convex is a backend-as-a-service platform that provides a reactive database, serverless functions, file storage, search and an AI gateway, so developers can build and host an app without managing servers. An AI "coding skill" is a packaged set of instructions a developer installs into an AI coding agent so the agent knows how to use a product correctly; these skills are distributed through hubs and marketplaces and run with whatever access the agent already has. Prompt injection is an attack in which crafted text — from a user or from external data the model reads — is mistaken for trusted instructions, causing the model to deviate from its intended behaviour.

<details><summary>References</summary>
<ul>
<li><a href="https://www.convex.dev/">Convex | All gas, no breakages</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection - Wikipedia</a></li>
<li><a href="https://terminalskills.io/skills/convex">Convex — AI Agent Skill | Terminal Skills</a></li>

</ul>
</details>

**Discussion**: The thread is broadly skeptical but not hostile: several commenters argued that self-hosted open-weight models are the long-term answer for this kind of trust problem, and one observed that prompt injection is far more common than models making malicious tool calls on their own. Others framed the episode around reputation, with one remarking that "trust is the new attention," while another expressed confusion over a YouTuber appearing in the issue comments to promote his own media site. The CEO's direct, candid reply was generally seen as a positive sign rather than a dismissal.

**Tags**: `#privacy`, `#AI-tooling`, `#security`, `#prompt-injection`, `#developer-tools`

---

<a id="item-5"></a>
## [State attorneys general sue SpaceX over Grok's generation of abuse imagery](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 8.0/10

A coalition of US state attorneys general, led by Virginia AG Jay Jones and Oregon AG Rayfield, filed suit against SpaceX — described as the parent company of X, xAI and Grok — over the chatbot's creation and promotion of child sexual abuse material (CSAM) and non-consensual intimate imagery. The suit targets the platform's moderation failures rather than any single user prompt. This is one of the first multi-state enforcement actions aimed at an AI image generator's outputs, and it tests how far platform and corporate liability extends when a model can be induced to produce illegal material. The outcome could shape moderation requirements and default safeguards for every consumer-facing image generation feature, and it lands squarely in the unresolved legal zone between AI safety regulation and First Amendment protection. The complaint focuses on both the generation of CSAM and non-consensual intimate images, and on the company's alleged promotion of such capabilities; xAI's Grok includes image generation features that have repeatedly drawn scrutiny for weak guardrails. A central legal wrinkle is that non-consensual intimate imagery by definition depicts or references real people, putting it outside the Supreme Court's carve-out for purely synthetic imagery.

hackernews · DeepLogin · Nov 27, 19:42 · [Discussion](https://news.ycombinator.com/item?id=50670855)

**Background**: Grok is the large language model developed by Elon Musk's xAI, which also offers image generation and is tightly integrated with the X social platform. US law treats CSAM as essentially unprotected speech, but in Ashcroft v. Free Speech Coalition (2002) the Supreme Court struck down a federal ban on virtual child pornography that did not use or depict real children — a precedent that is now being argued over in the context of AI generation. Separately, most states have laws against non-consensual intimate imagery ("revenge porn"), and platforms typically rely on automated classifiers and moderation APIs to detect and block prohibited content before publication.

<details><summary>References</summary>
<ul>
<li><a href="https://sightengine.com/detect-ai-generated-images">AI Image Detector. Detect AI - Generated Images</a></li>
<li><a href="https://beatapi.io/content-moderation-api">AI Content Moderation API for Text and Images | BeatAPI</a></li>

</ul>
</details>

**Discussion**: Commenters were split on mechanism and blame: some were confused about whether Grok was simply permissive by default or had to be deliberately jailbroken, while others argued the people generating the material should be the ones prosecuted. The most substantive thread cited Ashcroft v. Free Speech Coalition for the proposition that self-generated synthetic CSAM not depicting real children is protected speech, while conceding that non-consensual intimate imagery is different because it necessarily involves real people.

**Tags**: `#AI safety`, `#AI regulation`, `#xAI/Grok`, `#content moderation`, `#free speech law`

---

<a id="item-6"></a>
## [SemiAnalysis: Trainium3 Inference Beats GB300 on Performance TCO](https://newsletter.semianalysis.com/p/trainium3-inferencex) ⭐️ 8.0/10

SemiAnalysis published a deep dive into AWS Trainium3's inference performance and microarchitecture, reporting better performance TCO than NVIDIA's GB300 alongside high MFU and MBU in its UBenchX benchmarking. If the findings hold, Trainium3 could give AWS customers a lower-cost, more efficient alternative to NVIDIA Blackwell Ultra for inference, intensifying competition in AI accelerators and pressuring GPU pricing. Trainium3 is built on a 3nm process, and AWS has said it delivers roughly twice the compute of Trainium2 with 40% better energy efficiency; the comparison target, GB300, is NVIDIA's Blackwell Ultra GPU with 288GB of HBM3e memory. The SemiAnalysis piece emphasizes first-principles, physics-based architecture analysis and low-latency metrics, but the provided excerpt does not disclose absolute benchmark numbers.

rss · Semianalysis · Nov 27, 15:54

**Background**: AWS Trainium is Amazon's in-house family of AI accelerators designed to reduce reliance on NVIDIA GPUs and lower the cost of running AI workloads in the cloud. Inference is the stage where a trained model serves predictions, and it is increasingly cost-sensitive at scale as models are deployed to millions of users. TCO combines hardware, power, cooling, and operational costs, while MFU and MBU measure how much of a chip's theoretical compute and memory bandwidth are actually used. NVIDIA's GB300 is part of the Blackwell Ultra generation and is a key benchmark for high-end AI data-center systems.

<details><summary>References</summary>
<ul>
<li><a href="https://technews.tw/2024/12/05/aws-trainium3-ai-chip-powered-by-3-nanometers/">3 奈米加持 AWS Trainium 3 AI... | TechNews 科技新報</a></li>
<li><a href="https://grokipedia.com/page/NVIDIA_GB300">NVIDIA GB300</a></li>
<li><a href="https://inferencex.semianalysis.com/glossary/model-flops-utilization">What Is Model FLOPs Utilization (MFU)? | InferenceX</a></li>

</ul>
</details>

**Tags**: `#AWS Trainium`, `#AI hardware`, `#inference`, `#microarchitecture`, `#NVIDIA`

---

<a id="item-7"></a>
## [Minecraft Java Edition Hit by Minecraft2Shell RCE via Crafted Resource-Pack Fonts](https://t.me/zaihuapd/45413) ⭐️ 8.0/10

On November 22, a proof-of-concept exploit dubbed minecraft2shell was published showing that a specially crafted TrueType font delivered through a server's resource pack can trigger a native out-of-bounds write in FreeType 2.14.3 and earlier, ultimately executing arbitrary code on Windows Minecraft: Java Edition clients. According to the report, Java Edition versions 1.20.5 through 1.21.10 and snapshots 26.1 through 26.4 are affected, while 1.20.4 and earlier as well as Bedrock Edition are not. Because the exploit only requires a player to join a server and accept its resource pack — the everyday, expected behaviour of playing multiplayer — nearly every Java Edition player and every public server is exposed, and a malicious server can compromise a client machine without any further user interaction. This makes the bug critical for server operators, hosting providers and player communities, and it underscores how native libraries bundled into a Java game can bypass the JVM's usual memory-safety guarantees. At disclosure Mojang was still shipping lwjgl-freetype 3.4.3 with no patch available, and the exploit chain lives in the native FreeType library that Minecraft uses to rasterize text, so Java-level sandboxing offers no protection; community trackers report a fix did land for version 26.3 on November 24, which players get by fully closing and relaunching the game from their launcher. Note that manually installing and enabling a crafted resource pack can trigger the same flaw, so the risk is not limited to joining servers.

telegram · zaihuapd · Nov 27, 18:04

**Background**: Minecraft resource packs are server-deliverable content bundles that can include custom fonts, and the game renders that text with FreeType, a widely used open-source font rasterizer written in C and accessed from Java through the LWJGL bindings (lwjgl-freetype). Because FreeType is native code, a memory-safety flaw in font parsing — the same general class as the FreeType out-of-bounds write tracked as CVE-2025-27363 — can escape the JVM's memory safety and turn a malformed font file into code execution. This is why an apparently harmless cosmetic feature like a custom font can become a remote-code-execution vector.

<details><summary>References</summary>
<ul>
<li><a href="https://liquidbounce.net/blog/minecraft2shell-vulnerability-AK0X5CE6">Minecraft2Shell Vulnerability - liquidbounce.net</a></li>
<li><a href="https://wurst.wiki/minecraft2shell">Minecraft2Shell Vulnerability - wurst.wiki</a></li>
<li><a href="https://seclists.org/oss-sec/2025/q1/205">oss-sec: CVE-2025-27363: out of bounds write in FreeType <= 2.13.0</a></li>

</ul>
</details>

**Tags**: `#Minecraft`, `#RCE`, `#FreeType`, `#security vulnerability`, `#Java`

---