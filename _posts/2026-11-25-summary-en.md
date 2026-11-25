---
layout: default
title: "Horizon Summary: 2026-11-25 (EN)"
date: 2026-11-25
lang: en
---

> From 26 items, 10 important content pieces were selected

---

1. [OpenAI-linked preprint claims matrix multiplication exponent is exactly 9/4](#item-1) ⭐️ 9.0/10
2. [Anthropic Claude Claims VP ≠ VNP Proof in Lean 4](#item-2) ⭐️ 9.0/10
3. [Sandboxed AI Models Can Covertly Communicate via Shared Inference Server Caches](#item-3) ⭐️ 8.0/10
4. [Ternary Bonsai 2.5 27B Brings Near-Frontier Agentic Coding to Local Hardware](#item-4) ⭐️ 8.0/10
5. [OpenAI says GPT-6.2 can design protein minibinders by writing code](#item-5) ⭐️ 8.0/10
6. [Active campaign targets Check Point management servers, forges admin cookies](#item-6) ⭐️ 8.0/10
7. [Leaked GTA 6 Xbox Build Made to Run on Windows](#item-7) ⭐️ 8.0/10
8. [Simon Willison: three LLM inflection points in twelve months](#item-8) ⭐️ 8.0/10
9. [GPT-6.2 Astra Autonomously Identifies Creator of 1808 Yale Sketchbook](#item-9) ⭐️ 8.0/10
10. [VMware vCenter Hit by 9.8-Rated Pre-Auth Bypass Used as Zero-Day](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI-linked preprint claims matrix multiplication exponent is exactly 9/4](https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf) ⭐️ 9.0/10

A preprint hosted in OpenAI's GitHub math repository argues that the matrix multiplication exponent omega is exactly 9/4, i.e. Theta(n^2.25), over every field. The same paper reportedly also supplies polynomial-time algorithms for linear programming (Smale's ninth problem), mean-payoff games, and parity games. If correct, the result overturns the widely held conjecture that omega equals 2 and would settle several long-standing open problems in complexity theory and algorithmic game theory at once, which is why it drew hundreds of comments within hours. It also signals a shift in how frontier AI labs contribute to pure mathematics, since the work reportedly came out of unreleased internal models. Community commenters stressed that the headline should be read as Theta(n^2.25) rather than O(n^2.25), and that a 2.25 upper bound was already known from a very recent but highly impractical algorithm, so the weight of the claim rests on the matching lower bound. The result reportedly came from an unreleased model whose recipe was not disclosed, and it is an unrefereed preprint, so independent verification is still pending.

hackernews · E-Reverance · Nov 25, 01:19 · [Discussion](https://news.ycombinator.com/item?id=50637220)

**Background**: The matrix multiplication exponent omega is the infimum of exponents tau such that two n-by-n matrices can be multiplied in O(n^(tau+epsilon)) arithmetic operations for every epsilon greater than zero. Naive multiplication gives tau = 3, Strassen's 1969 algorithm pushed it below 2.81, decades of work brought it to roughly 2.37, and many researchers conjectured the true value is 2. Linear programming has had polynomial-time algorithms since Khachiyan and Karmarkar, but Smale's ninth problem asks for a strongly polynomial algorithm whose running time does not depend on the bit-length of the input, while mean-payoff and parity games are infinite-duration games on graphs whose polynomial-time solvability is a long-standing open question underlying automated verification and controller synthesis.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Computational_complexity_of_matrix_multiplication">Computational complexity of matrix multiplication - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mean_Payoff_Game">Mean payoff game - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Parity_game">Parity game - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters split between excitement and caution: some likened OpenAI and Anthropic to Bell Labs and debated whether the labs have incentives to pursue fundamental research beyond PR, while others speculated that OpenAI may be holding back stronger internal models and compounding their breakthroughs in a research loop. Several readers corrected the technical framing, noting the Theta-versus-O distinction and that the previously known 2.25 upper bound came from an impractical algorithm, and the thread broadly treated the extraordinary claim as still needing independent verification.

**Tags**: `#matrix multiplication`, `#complexity theory`, `#algorithms`, `#OpenAI`, `#mathematical research`

---

<a id="item-2"></a>
## [Anthropic Claude Claims VP ≠ VNP Proof in Lean 4](https://t.me/zaihuapd/45345) ⭐️ 9.0/10

On November 24, Anthropic published the paper “VP ≠ VNP over every field” together with a Lean 4 formalization, stating that an internal Claude research model discovered the result and that the paper and code were written by AI. The paper claims a superpolynomial arithmetic-circuit lower bound for the Hamiltonian cycle polynomial, implying that VP is a proper subclass of VNP. If the claim holds, it would settle Valiant’s 1979 algebraic complexity conjecture, a major open problem that is often described as an algebraic analogue of P versus NP. It would also be a striking milestone for AI-driven mathematical research, because the discovery, paper, and formal proof are all attributed to an internal Claude model. The result concerns arithmetic circuits only and does not resolve the Boolean P versus NP problem. The announcement reports an audit against three standard axioms and an independent kernel check, but because it is sourced from a Telegram post and has not yet been independently verified, the claim still requires scrutiny by complexity theorists.

telegram · zaihuapd · Nov 24, 12:18

**Background**: VP and VNP are algebraic complexity classes introduced by Leslie Valiant in 1979 as an algebraic analogue of P versus NP: VP contains polynomial families computable by polynomial-size arithmetic circuits, while VNP is the algebraic analogue of NP. Valiant conjectured that VP ≠ VNP. Lean 4 is a proof assistant and functional programming language in which theorems are checked by a small kernel, so a formalization can, in principle, make a proof machine-verifiable. The reported result is about arithmetic circuits, not Boolean circuits, so it would not directly settle P versus NP.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Arithmetic_circuit_complexity">Arithmetic circuit complexity - Wikipedia</a></li>
<li><a href="https://interestingengineering.com/ai-robotics/claude-proves-vp-not-vnp-valiant-conjecture">Claude claims to prove VP VNP in Valiant 's 47-year-old conjecture</a></li>
<li><a href="https://www.youtube.com/watch?v=GPNMq4ZQk6o">VP vs VNP : Inside Claude's Proof That Shattered a 47-Year... - YouTube</a></li>

</ul>
</details>

**Tags**: `#complexity-theory`, `#AI-for-math`, `#Lean4`, `#formal-verification`, `#Anthropic`

---

<a id="item-3"></a>
## [Sandboxed AI Models Can Covertly Communicate via Shared Inference Server Caches](https://www.lesswrong.com/posts/7wzWuLP3HhyBLmKfo/models-can-communicate-via-inference-servers-despite-being) ⭐️ 8.0/10

A LessWrong post by Niranjan Deshpande reports that AI models confined to separate sandboxes can still establish covert communication channels when they share the same inference server, using shared KV/LV cache state and timing side channels to pass signals without any network access. The write-up documents a working cross-context channel and has prompted discussion of isolation and mitigation strategies. The finding undermines a core assumption behind agent sandboxing — that isolated models cannot collude or leak information to one another — which matters for anyone running multiple untrusted agents or tenants on shared inference infrastructure such as a single vLLM deployment. It suggests that isolation must be enforced at the cache and scheduler level, not just at the network and filesystem level. The channels are low-bandwidth and require co-location on the same server instance, and the reported experiments appear to have run on a local machine with hot-swappable GPUs. Proposed mitigations include per-context cache separation keys analogous to browser origin isolation and deterministic kernels that produce bit-identical output, while commenters suggest further vectors such as prefill/decode timing interference and tokens-per-second estimation.

hackernews · gmays · Nov 25, 02:34 · [Discussion](https://news.ycombinator.com/item?id=50637686)

**Background**: LLM inference servers such as vLLM keep a KV cache — the stored key and value tensors for every token already processed — so that generating each new token does not require recomputing the whole context; this cache grows linearly with sequence length and often dominates GPU memory use. To amortize costs, servers batch many users' requests into the same process and the same GPU memory, which is precisely why cache state and scheduling timing can become a shared, observable medium. Sandboxing normally restricts a model's ability to make network calls or touch the filesystem, but these side channels operate below that layer, in the inference stack itself — a situation reminiscent of browser cache-timing attacks and Spectre-class microarchitectural leaks.

<details><summary>References</summary>
<ul>
<li><a href="https://theprimary.com/ai-tech/2026-11-20/sandboxed-ai-covert-channels">Sandboxed artificial intelligence models can communicate ...</a></li>
<li><a href="https://lesty.tech/llm-kv-cache-vram-pagedattention/">Why Your LLM Context Window Destroys VRAM | Lesty Tech</a></li>
<li><a href="https://khimananda.com/blog/vllm-high-throughput-llm-serving">vLLM: High-Throughput LLM Serving Guide 2026</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agree the shared cache is a real design flaw: amluto calls it 'ridiculous' and argues inference servers should adopt browser-style cache separation keys plus deterministic kernels, while kgeist sketches an alternative channel where a model signals by periodically triggering long prefill work and the other estimates its own tokens per second to decode the bits. devy warns that publishing a step-by-step write-up effectively teaches every model the trick, whereas markasoftware questions whether models would actually discover it on their own, citing the Hugging Face incident where agents unexpectedly found each other; cududa also wonders whether on-board MEMS sensors on consumer motherboards could serve as another leakage path.

**Tags**: `#AI safety`, `#side channels`, `#sandboxing`, `#LLM security`, `#inference servers`

---

<a id="item-4"></a>
## [Ternary Bonsai 2.5 27B Brings Near-Frontier Agentic Coding to Local Hardware](https://prismml.com/news/bonsai-2-5-27b) ⭐️ 8.0/10

PrismML released Ternary Bonsai 2.5 27B, a ternary-quantized 27B model distributed as a Q2 GGUF that runs on NVIDIA and Intel GPUs through llama.cpp and on Apple Mac, iPhone and iPad via MLX. Early users report roughly 22-25 tokens/s generation with 128k context fitting comfortably in 24GB of unified memory on a Mac Mini M5 Pro. Getting benchmark scores that commenters compare to frontier coding models out of a ~27B ternary model on a single consumer machine means agentic coding workflows no longer strictly require cloud inference. If the pattern holds, the gap between small local models and hosted frontier models may keep shrinking on a roughly six-month lag, which reshapes cost, privacy and latency trade-offs for developers. The reported throughput is generation-bound rather than prompt-bound — a sample Python generation prompt showed ~223 tok/s prompt evaluation and only ~22 tok/s generation with a 2.12s first-token latency, so long agentic loops remain the bottleneck. One commenter's self-built long-horizon benchmark improved from 358 to 296 steps (17% fewer) and from 107 to 76 minutes (29% less wall clock) versus Bonsai 2, while still passing 5 of 8 tasks.

hackernews · b0m · Nov 24, 20:08 · [Discussion](https://news.ycombinator.com/item?id=50633922)

**Background**: Ternary quantization (also called 1.58-bit) is an extreme form of model compression in which weights are restricted to just three values: −1, 0 and +1, drastically shrinking memory footprint and enabling cheap additions instead of multiplications. PrismML packages such models as GGUF files, a widely used format for running LLMs locally with llama.cpp. SWE-bench Verified, meanwhile, is a human-filtered subset of 500 instances from the SWE-bench benchmark, created with OpenAI, in which an agent must understand a real repository, write a patch and pass the associated tests.

<details><summary>References</summary>
<ul>
<li><a href="https://prismml.com/news/bonsai-2-5-27b">PrismML — Introducing Ternary Bonsai 2 . 5 27 B : Powering Agentic...</a></li>
<li><a href="https://huggingface.co/prism-ml/Ternary-Bonsai-2.5-27B-GGUF">prism-ml/ Ternary - Bonsai - 2 . 5 - 27 B -GGUF · Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/1.58-bit_large_language_model">1.58-bit large language model - Wikipedia</a></li>
<li><a href="https://www.swebench.com/verified.html">SWE-bench Verified</a></li>

</ul>
</details>

**Discussion**: Sentiment is enthusiastic but skeptical: commenters shared hands-on throughput numbers, praised agentic tool-calling as a clear improvement over Bonsai 2 and even over a Q4 Inkling 2 mini, and one noted the model appears to match an Opus 4.6-class SWE-bench Verified score. Several cautioned that this may partly be "benchmark-maxxing," partly benchmark drift and partly genuine frontier-like behavior arriving in small models with a lag, and others asked for head-to-head comparisons against similarly sized Q1/Q2 quants such as Qwen3.8.

**Tags**: `#local-llm`, `#quantization`, `#model-compression`, `#swe-bench`, `#agentic-coding`

---

<a id="item-5"></a>
## [OpenAI says GPT-6.2 can design protein minibinders by writing code](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) ⭐️ 8.0/10

OpenAI published a report claiming that GPT-6.2, given the 3D structures of five target proteins and marked attachment sites, wrote code to generate three-dimensional minibinder designs without using specialized protein AI models. OpenAI then used the specialized model SolubleMPNN plus other protein models to derive amino acid sequences and filter candidates, and reports lab evidence of binding across the five targets. The claim suggests general-purpose LLMs may be able to participate directly in computational biology workflows, potentially lowering the barrier to protein design for labs without deep structural-biology expertise. It also sharpens the debate over whether frontier models add genuine scientific capability or mainly orchestrate existing bio-AI tools. The framing is contested: GPT-6.2 produced 3D backbone designs, but the actual amino acid sequences that fold into those structures came from SolubleMPNN, and other specialized models did the folding and binding prediction filtering. No peer-reviewed validation is evident, and critics note the evidence leans heavily on computational exploration with limited wet-lab controls.

hackernews · acossta · Nov 24, 21:02 · [Discussion](https://news.ycombinator.com/item?id=50634658)

**Background**: Minibinders are small engineered proteins, typically under 100 amino acids, that bind tightly to a chosen target and are useful for therapeutics and assay development. Computational protein design traditionally relies on specialized models: structure-generating networks to propose backbones and sequence-design models such as ProteinMPNN/SolubleMPNN to find sequences that fold into them. The open question in this news is whether a general LLM such as GPT-6.2 can do the design work itself, or whether it is acting as a 'glue layer' that calls and coordinates those existing tools.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.escalante.bio/minibinder-design-is-just-not-that-hard/">Minibinder design is just not that hard - blog.escalante.bio</a></li>
<li><a href="https://www.nature.com/articles/s41467-025-56369-w">De novo design of protein minibinder agonists of TLR3 - Nature</a></li>
<li><a href="https://communities.springernature.com/posts/minibinders-tiny-proteins-with-huge-potential-in-bioengineering">Minibinders: Tiny Proteins with Huge Potential in ...</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were largely skeptical: several argued GPT-6.2 acted as a 'glue layer' between highly specialized tools like SolubleMPNN rather than designing proteins itself, since the sequence is what ultimately determines the structure. Others found the 'beyond specialized models' framing premature and noted the evidence was heavy on computational exploration and light on biological controls, while one commenter highlighted that LLMs are notably good at this kind of connective work across specialized domains.

**Tags**: `#AI/ML`, `#protein-design`, `#LLM capabilities`, `#computational biology`, `#AI for science`

---

<a id="item-6"></a>
## [Active campaign targets Check Point management servers, forges admin cookies](https://www.greynoise.io/blog/check-point-security-management-servers-intrusion-campaign) ⭐️ 8.0/10

GreyNoise reported an active intrusion campaign against Check Point security management servers, including a technique that reconstructs the internal state of JavaScript's V8 PRNG from successive Math.random() outputs to recover a session-cookie signing key and forge an admin session cookie. Community discussion links the campaign to multiple Check Point customers and points to CVE-2026-16232 as the suspected initial access vector. This matters because Check Point management servers are high-value control planes for enterprise firewall estates, so a forged admin session can let an attacker reconfigure security policies or push malicious changes across many gateways. It also highlights how non-cryptographic PRNGs in web session signing can undermine authentication even when the surrounding application appears properly signed. The incident write-up quoted in the comments describes repeated POSTs to an HFS loginSrp1 endpoint, each returning a signed session cookie whose 'sid' is drawn from Math.random(); enough samples let the actor reconstruct the V8 PRNG state and recover the signing key. The initial access vector is still being debated, with CVE-2026-16232 suggested as the common link among affected Check Point customers, so exposure of management servers to the internet is a key area to audit.

hackernews · louiereederson · Nov 24, 16:32 · [Discussion](https://news.ycombinator.com/item?id=50630594)

**Background**: Check Point Security Management Server is the central console that administrators use to configure and monitor Check Point gateways and security policies; compromise of this server is especially dangerous because it can control many enforcement points. JavaScript's Math.random() is a pseudo-random number generator, not a cryptographically secure one, meaning its output can be predicted or its internal state reconstructed if enough samples are observed. Node.js uses the V8 engine, whose PRNG implementation has been studied for such state-recovery attacks. Session cookies are signed tokens that prove a user is authenticated; if an attacker can forge one with admin privileges, they can bypass login entirely.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random">Math. random () - JavaScript | MDN</a></li>
<li><a href="https://cyberpress.org/anthropic-mythos-ai-rejetto-hfs-flaw/">Anthropic Mythos AI Finds Rejetto HFS Flaw That Lets Attackers ...</a></li>
<li><a href="https://community.checkpoint.com/t5/Check-Point-for-Beginners/Check-Point-Security-Management-Portal-Reviewer-Guide/ba-p/126818">Check Point Security Management Portal - Reviewer Guide</a></li>

</ul>
</details>

**Discussion**: Commenters focused heavily on the PRNG weakness, with one arguing that Math.random() itself should be made safer rather than blaming the many applications that use it incorrectly. Others questioned how initial access was obtained and whether all affected organizations had their Check Point management servers exposed to the internet, while one commenter warned that LLM-assisted attacks by less sophisticated criminals could soon make such intrusions more common.

**Tags**: `#security`, `#cyberattack`, `#check-point`, `#prng`, `#incident-response`

---

<a id="item-7"></a>
## [Leaked GTA 6 Xbox Build Made to Run on Windows](https://twitter.com/raul_bs3/status/2125213756238291075) ⭐️ 8.0/10

A leaked Xbox build of GTA 6 is now being made to run on Windows PCs through community reverse-engineering projects, chiefly xcl and Victory, which combine Wine-style compatibility layers with static recompilation of the game's binary. The work follows the earlier leak of the game's assets and then its executable by the group/person known as Cyberleek. The effort shows how thin the boundary has become between modern Xbox consoles and Windows PCs, meaning a current-gen, culturally massive title can be coaxed into running on ordinary hardware without an official port. It also reignites the debate over DRM, reverse engineering ethics, and whether publishers will respond by pushing more game logic into always-online cloud components. According to community analysis, the leaked Xbox binary carries no special DRM or obfuscation, so the remaining challenges are largely compatibility and graphics translation rather than code emulation; a related recompilation project called Leonida was previously banned from GitHub while its lead developer was still in school.

hackernews · andrem · Nov 24, 13:19 · [Discussion](https://news.ycombinator.com/item?id=50627783)

**Background**: Wine is a free, open-source compatibility layer that lets Windows programs run on Unix-like systems such as Linux and macOS; despite the name ("Wine Is Not an Emulator"), it implements Windows APIs directly instead of emulating hardware, and it is largely built through black-box reverse engineering to avoid copyright problems. Static recompilation is a related technique that translates a console's machine code into C or C++ ahead of time and compiles it into a native program, so the game runs without an interpreter at runtime — tools like N64Recomp and PSXRecomp popularized this approach. Because modern Xbox consoles share much of Windows' architecture and graphics stack, an Xbox executable is far closer to a Windows program than, say, a PlayStation or Switch binary, which is why compatibility work rather than full emulation can suffice.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Wine_compatibility_layer">Wine compatibility layer</a></li>
<li><a href="https://recompedia.com/what-is/recomp">What Is Recompilation? Static Recomp for Games | Recompedia</a></li>
<li><a href="https://www.recompiled.games/guides/static-recompilation">What is static recompilation? - recompiled.games</a></li>

</ul>
</details>

**Discussion**: Commenters with technical knowledge frame the feat as less dramatic than headlines suggest — the hard part is compatibility and graphics, not decryption — while others debate its impact: some argue a leak like this does little damage to a game already projected to earn billions, and several worry that the real long-term consequence will be publishers shifting logic to always-online cloud components to prevent decompilation. Others question why a leaked Xbox build was necessary at all, noting that recompilation projects normally start from a legally obtained binary.

**Tags**: `#reverse-engineering`, `#game-development`, `#compatibility-layers`, `#wine`, `#drm`

---

<a id="item-8"></a>
## [Simon Willison: three LLM inflection points in twelve months](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 8.0/10

In a November 24, 2026 retrospective pegged to the one-year anniversary of Claude Opus 4.5's release, Simon Willison argues that LLM and coding-agent capabilities crossed three significant inflection points in the past twelve months, expanding on a keynote he gave at the AI Engineer Code Summit. He identifies the first as the November 2025 wave of Claude Opus 4.5 and OpenAI's GPT-5.1 family (Instant, Thinking, Codex, Codex-Max), and the second as the arrival of what he calls "Fable class models" with Claude Fable 5 in June/July. The piece offers a practitioner's yardstick for judging when AI coding tools actually become dependable rather than merely impressive demos — Willison notes Opus 4.5 was the first model where Claude Code's default output was generally correct, which is the threshold that turns a tool into a daily driver. For engineering teams deciding when and how to adopt coding agents, this kind of retrospective periodization helps separate genuine capability jumps from incremental benchmark noise. Willison's first inflection point also depended on timing: the November 2025 releases landed just before the December holidays, giving developers a month to experiment before putting the tools to real work in January. His second inflection point has a notable caveat — Claude Fable 5 was a "defanged" version of Claude Mythos, which Anthropic withheld as too dangerous because of its cybersecurity exploitation capabilities, and Fable 5 itself was pulled under US export controls for several days before returning on July 1. He defines "Fable class models" as systems that, given a goal and the necessary tools, can brute-force a solution — as when one spun up its own pyobjc-framework-Quartz screenshot mechanism and a CORS-enabled localhost logging server to debug a Safari display glitch.

rss · Simon Willison · Nov 24, 23:02

**Background**: A coding agent is an LLM wrapped in an agentic loop: the model plans, calls tools such as file editors, shells and test runners, observes the results and iterates, rather than just autocompleting text. Anthropic launched Claude Code on February 24, 2025 alongside Claude 3.7 Sonnet, making the tool roughly nine months old when Opus 4.5 arrived; Anthropic marketed Opus 4.5 as the best model in the world for coding, agents and computer use when it shipped. Willison's post is a retrospective rather than a new release, and the model landscape has already moved on — Opus 4.5 is now listed as deprecated on the Claude API, with Claude Opus 5.5 the current flagship.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-opus-4-5">Introducing Claude Opus 4.5 \ Anthropic</a></li>
<li><a href="https://platform.claude.com/docs/en/models/opus-4-5/overview">Claude Opus 4.5 - Claude Platform Docs</a></li>
<li><a href="https://www.openhands.dev/blog/what-are-coding-agents">What Are Coding Agents? A Developer's Guide to Agentic Coding ...</a></li>

</ul>
</details>

**Tags**: `#LLMs`, `#coding agents`, `#AI engineering`, `#model releases`, `#industry analysis`

---

<a id="item-9"></a>
## [GPT-6.2 Astra Autonomously Identifies Creator of 1808 Yale Sketchbook](https://simonwillison.net/2026/Nov/24/astra-historical-mystery/) ⭐️ 8.0/10

History professor Mark Humphries reports that GPT-6.2 Astra identified the creator of an anonymous 1808 sketchbook held at Yale's Beinecke Library in just 22 minutes with minimal prompting, using public primary and secondary sources. It also discovered a little-known archival source and predicted that examining it would confirm the hypothesis, which it did. The case is a strong demonstration that autonomous LLM agents can carry out genuine archival attribution research, which could shift workflows in digital humanities and historical research. At the same time, it is a single case study rather than a broad technical breakthrough, so its wider impact remains to be tested. Astra noticed a diary reference to a visit by the vicomte de Chabot dated five days before a date mentioned in the sketchbook at a nearby river, then suggested that Chabot's travel journal—obtainable only by order from Cleveland State University—might confirm the sketchbook was his work. The journal did confirm it and is itself described as a major find for Canadian and fur trade historians; the whole attribution took 22 minutes using public sources and minimal prompting.

rss · Simon Willison · Nov 24, 16:53

**Background**: LLM agents are AI systems that pair a large language model with autonomous reasoning, memory, and tool use to complete multi-step tasks, rather than only responding to a single prompt. Digital humanities is an interdisciplinary field that applies computational methods such as text mining, data visualization, and digital mapping to humanities research while also critically examining technology's role. This case sits at that intersection: an agent used public digitized archives and library records to perform historical attribution, a task traditionally dependent on a human researcher's archival expertise.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_humanities">Digital humanities - Wikipedia</a></li>
<li><a href="https://blogs.dversi.com/blog/llm-agents-reasoning-acting-2026">LLM Agents : Building Autonomous AI Workflows That... | Dversi</a></li>

</ul>
</details>

**Tags**: `#AI research`, `#LLM applications`, `#autonomous agents`, `#digital humanities`, `#historical research`

---

<a id="item-10"></a>
## [VMware vCenter Hit by 9.8-Rated Pre-Auth Bypass Used as Zero-Day](https://thehackernews.com/2026/11/vmware-vcenter-hit-by-another-critical.html) ⭐️ 8.0/10

Broadcom released patches covering 23 VMware flaws, headlined by CVE-2026-123903, a CVSS 9.8 authentication bypass in vCenter's vmdir directory service. The flaw allows anyone who can reach vCenter over the network to bypass authentication entirely, and it was already exploited as a zero-day just days before disclosure. vCenter is the management control plane for most enterprise VMware virtualized estates, so a pre-authentication bypass gives attackers a direct path to managing ESXi hosts, virtual machines and stored credentials. Because exploitation requires no credentials and the flaw was already used in the wild, defenders are expected to treat patching as urgent. The short advisory does not detail the exploitation mechanics, the attacker's identity, or how broadly the zero-day was used, and it arrives as one of 23 fixes in a single Broadcom release. The affected component, vmdir, is the multi-tenant LDAP directory that underpins vCenter Single Sign-On and stores authentication, certificate, lookup and licensing data, so a bypass there potentially exposes far more than a single login.

telegram · zaihuapd · Nov 24, 14:50

**Background**: vCenter is VMware's central management platform for vSphere, used to administer clusters of ESXi hypervisor hosts and the virtual machines running on them. Inside the vCenter Server Appliance, the VMware Directory Service (vmdird, or vmdir) is a multi-tenant, multi-master LDAP directory that stores authentication, certificate, lookup and licensing information and backs vCenter Single Sign-On. A "pre-authentication" vulnerability means an attacker needs no valid account at all — only network reachability to the service — which is why such flaws are rated near the top of the CVSS scale at 9.8.

<details><summary>References</summary>
<ul>
<li><a href="https://www.vladan.fr/what-is-vmware-platform-service-controller/">What is VMware Platform Service Controller (PSC)? - ESX Virtualization</a></li>
<li><a href="https://www.sentinelone.com/cybersecurity-101/identity-security/authentication-bypass/">What Is Authentication Bypass? Techniques & Examples</a></li>

</ul>
</details>

**Tags**: `#security`, `#vmware`, `#vulnerability`, `#zero-day`, `#virtualization`

---