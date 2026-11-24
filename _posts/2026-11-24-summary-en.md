---
layout: default
title: "Horizon Summary: 2026-11-24 (EN)"
date: 2026-11-24
lang: en
---

> From 35 items, 6 important content pieces were selected

---

1. [Nvidia Board Reinstates Jensen Huang as CEO After Government Input](#item-1) ⭐️ 9.0/10
2. [Ladybird, the from-scratch browser engine, enters alpha](#item-2) ⭐️ 8.0/10
3. [Zhipu AI releases GLM-5.4, its first looped-transformer model for coding](#item-3) ⭐️ 8.0/10
4. [Codex2api Supply-Chain Attack: Backdoored Releases via Compromised Author Account](#item-4) ⭐️ 8.0/10
5. [ChatGPT adds GPT-6.2 Sol to chat tab, rolling out to paid users](#item-5) ⭐️ 8.0/10
6. [Anthropic says internal Claude model proved VP ≠ VNP, with Lean 4 formalization](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Nvidia Board Reinstates Jensen Huang as CEO After Government Input](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html) ⭐️ 9.0/10

Nvidia’s board reinstated Jensen Huang as president, CEO, and board director, less than two weeks after his departure, saying it had received input from senior U.S. government officials and concluded his return poses no national security risk. The reversal puts a spotlight on Nvidia’s founder-dependent governance and on how national-security concerns around AI chips can draw the U.S. government into a major public company’s leadership decisions, with implications for investors, export-control policy, and the semiconductor industry. The board’s statement, as quoted by commenters, says the input came from “senior levels of the United States government”; governance experts cited in coverage question board independence and say Huang is “too big to fire.” The episode also follows earlier scrutiny of Nvidia and U.S. export controls on advanced chips to China.

hackernews · jaz · Nov 23, 14:00 · [Discussion](https://news.ycombinator.com/item?id=50611576)

**Background**: Nvidia is a leading designer of GPUs used for AI training and data-center workloads, making it central to U.S. technology policy. Washington has tightened export controls on advanced semiconductors to China on national-security grounds, and chipmakers’ compliance is politically sensitive. Corporate governance generally gives a board authority to hire and fire the CEO, but founder-led firms can concentrate influence in ways that test board independence.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnn.com/2026/11/23/tech/nvidia-reinstates-jensen-huang-corporate-governance">Nvidia’s $1.5 trillion boardroom blunder helped bring Jensen ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/24/nvidia-jensen-huang-governance.html">Jensen Huang is ‘too big to fire,’ putting Nvidia’s ...</a></li>
<li><a href="https://www.semiconductors.org/policies/export-control-and-national-security-policy/">Export Control | SIA | Semiconductor Industry Association</a></li>

</ul>
</details>

**Discussion**: Commenters focused on the statement that the board received input from senior U.S. government officials, seeing it as the key signal of political involvement. Some debated whether the board’s rapid reversal and unanimity undermine accountability, while others argued there is no evidence of wrongdoing and criticized perceived hypocrisy in export-control enforcement. Several drew parallels to OpenAI’s 2023 board crisis, arguing that formal governance structures may not reflect real power.

**Tags**: `#Nvidia`, `#Jensen Huang`, `#corporate governance`, `#national security`, `#semiconductors`

---

<a id="item-2"></a>
## [Ladybird, the from-scratch browser engine, enters alpha](https://ladybird.org/posts/alpha/) ⭐️ 8.0/10

Ladybird, an open-source browser engine written from scratch, has shipped its first alpha release for macOS and Linux after roughly four years of independent development. The release marks the first time users and testers can broadly try the engine and file feedback before a stable version. Almost the entire web is rendered by a handful of engines—Blink, Gecko and WebKit—each backed by a company with its own commercial agenda, so a genuinely independent engine offers a check on that concentration. Early user reports that real-world sites render correctly suggest the project has moved from a technical curiosity to a credible long-term alternative. The alpha is limited to macOS and Linux, so it is not yet a daily-driver replacement for most people, and users note rough edges such as slightly jerky page scrolling. Ladybird has also moved away from some of its own hand-rolled libraries in favor of production-grade ones like SQLite and Skia, a change credited with substantially improving rendering quality.

hackernews · janvdberg · Nov 23, 16:13 · [Discussion](https://news.ycombinator.com/item?id=50614249)

**Background**: A browser engine is the core component that fetches a web page, parses its HTML, CSS and JavaScript, and lays it out on screen—it is the part of a browser that actually decides what a site looks like. Ladybird began life as a component of SerenityOS, a hobby operating system, before spinning out into its own project run by the nonprofit Ladybird Browser Initiative and funded entirely by donations, with sponsors including Cloudflare, FUTO, Shopify, Proton and 37signals. It is licensed under the permissive BSD 2-Clause License.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ladybird_(web_browser)">Ladybird (web browser) - Wikipedia</a></li>
<li><a href="https://ladybird.org/">Ladybird</a></li>
<li><a href="https://en.wikipedia.org/wiki/Browser_engine">Browser engine - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were largely enthusiastic, with several reporting that tricky real-world sites—including heavy news sites and Proxmox's noVNC web console—rendered correctly and even felt snappier than in Firefox. The main concern raised was privacy: one commenter urged Ladybird to take fingerprinting seriously via a non-compliant JS mode with spoofed or randomized values and far more granular permissions, while another asked what security precautions early users should take. A few voiced nostalgia for the original SerenityOS hacker spirit now that the project leans on established third-party libraries.

**Tags**: `#browsers`, `#Ladybird`, `#web engines`, `#open source`, `#software releases`

---

<a id="item-3"></a>
## [Zhipu AI releases GLM-5.4, its first looped-transformer model for coding](https://z.ai/blog/glm-5.4) ⭐️ 8.0/10

Zhipu AI released GLM-5.4, described as its first flagship "Loop Transformer" model aimed at generalized coding tasks such as generating video, games, CAD models and GLSL shaders through code. Instead of stacking unique layers, the model runs a shared block of layers for multiple iterations, which Z.ai claims gives reasoning depth comparable to 2T–3T parameter models without adding parameters. This is one of the first production-scale deployments of looped/recurrent-depth architecture from a major Chinese lab, marking a shift away from pure parameter scaling toward reusing compute at inference time. If the approach holds up, it could lower memory-bandwidth pressure and change how open coding models are priced and compared against frontier systems. GLM-5.4 loops a shared 28-layer block twice rather than running a taller stack of distinct layers, and Z.ai says it consumes roughly one-third fewer credits than GLM-5.3 for the same token volume, with Coding Plan pricing starting at about US$18 per month. Access is a practical caveat: the model was not available through OpenRouter or the standard Z.ai API plan at launch, only via the Coding Plan, whose API keys behave like regular ones but reach the new model.

hackernews · foohis · Nov 23, 10:06 · [Discussion](https://news.ycombinator.com/item?id=50609685)

**Background**: A looped transformer (also called recurrent depth or looped depth sharing) applies the same transformer block repeatedly, feeding hidden states from one pass into the next, so a model gains "depth" of computation without gaining parameters — an idea tracing back to the Universal Transformer. This matters for inference economics because the main bottleneck in serving LLMs is memory bandwidth: each layer's weights must be shuttled from HBM into the chip, computed once, then swapped out. Reusing the same weights across loop iterations means fewer distinct weight transfers per generated token.

<details><summary>References</summary>
<ul>
<li><a href="https://anyrouter.dev/model/z-ai/glm-5.4">GLM - 5 . 4 · Zhipu AI · pricing & API · AnyRouter</a></li>
<li><a href="https://sebastianraschka.com/llm-architecture-gallery/looped-depth-sharing/">Looped Transformer | Sebastian Raschka, PhD</a></li>
<li><a href="https://kingy.ai/blog/glm-5-4-launch/">GLM ‑ 5 . 4 launch: How to use it, pricing and API status</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were largely positive on Zhipu's transparency, with one top commenter framing the original Transformer as an "unrolled for loop" that unnaturally pairs separate attention and feed-forward weight sets, and another explaining the loop design as a direct attack on the HBM memory-bandwidth bottleneck. Simon Willison shared hands-on pelican SVG tests for low/high/max reasoning settings and flagged the awkward Coding-Plan-only access, while a dissenting commenter complained that Chinese models' "marathon thinking" makes even trivial tasks slow, suspecting it is how they close the gap on benchmarks.

**Tags**: `#llm`, `#loop-transformer`, `#model-release`, `#glm`, `#hacker-news`

---

<a id="item-4"></a>
## [Codex2api Supply-Chain Attack: Backdoored Releases via Compromised Author Account](https://github.com/WormW/codex2api-incident-2026-11) ⭐️ 8.0/10

The Codex2api author's GitHub account was compromised, and the attacker pushed tags outside the main branch to publish backdoored releases v3.1.10 through v3.1.12. Version 3.1.11 removed authentication entirely, enabling unauthenticated remote code execution, while an injected workflow exfiltrated 16 GitHub Actions secrets across at least 21 repositories under the same account. Anyone running an affected Codex2api instance should assume full host and credential compromise, since the backdoor grants unauthenticated command execution and the leaked secrets can be used to pivot into other repositories and services. The incident is also a broadly instructive case study in release/tag-based supply-chain risk: branch protection on main does not necessarily cover tag-triggered release workflows. Affected users should immediately stop the service, roll back to v3.1.9, and rotate the GitHub token, SSH keys, database credentials, and DeepSeek and other API keys referenced by the deployment. The attacker never needed to touch main; pushing tags was enough to make the release pipeline build and ship the malicious artifacts.

telegram · zaihuapd · Nov 23, 11:21

**Background**: Codex2api is a Go + Gin / React + Vite reverse-proxy gateway that wraps local Codex runtimes into a private multi-account API service with a web dashboard, so its users typically hold real credentials for upstream model APIs and databases. GitHub Actions secrets are encrypted values stored at repository, environment, or organization scope and injected into workflows; once a workflow is modified, it can read and send those secrets outward. Branch protection rules usually guard commits to branches, but release pipelines triggered by tag pushes are a separate path that must be protected explicitly.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/cherry-ff/codex2api/blob/main/README.md">codex2api/README.md at main · cherry-ff/codex2api · GitHub</a></li>
<li><a href="https://github.com/features/actions">GitHub Actions · CI/CD and automations · Agentic Workflows...</a></li>

</ul>
</details>

**Discussion**: Discussion comes from a Telegram channel rather than a threaded technical forum, so it is limited to an urgent heads-up telling anyone who updated Codex2api that afternoon to check immediately. There is no substantive debate over the root cause or remediation in the provided comments.

**Tags**: `#supply-chain-security`, `#github-actions`, `#backdoor`, `#incident-response`, `#secrets-management`

---

<a id="item-5"></a>
## [ChatGPT adds GPT-6.2 Sol to chat tab, rolling out to paid users](https://x.com/ChatGPT/status/2124942186425069836) ⭐️ 8.0/10

ChatGPT's official account announced on November 23 that a GPT-6.2 Sol version is now live on the Chat tab, aimed at everyday conversation, and is being rolled out starting that day to Plus, Pro, Business and Enterprise subscribers. OpenAI says the new version handles complex requests better — especially detailed multi-part instructions or requests that require searching the web — and improves recognition of photo details such as label text and road signs, filtering online options by priorities like price or location, and judging when to proactively offer follow-up suggestions. A new model being pushed to the default chat surface — rather than only through the API or a separate model picker — means hundreds of millions of paying users will feel the change in their daily conversations, and it signals how OpenAI is positioning its model family: Sol for everyday use versus the heavier Astra tier. Improvements in image-detail reading and proactive follow-up suggestions point toward ChatGPT behaving more like an agent that anticipates the next step rather than a pure question-answer box. The capability claims come entirely from OpenAI's own announcement and have not been independently verified, and the source item is a brief repost from a Telegram channel rather than a full technical post. Notably, the announcement describes a rollout to the chat tab on November 23, whereas public records indicate GPT-6.2 Astra and Sol first launched on November 17 and were already restricted to paid tiers, so the news is better read as an expansion of availability than a brand-new model release.

telegram · zaihuapd · Nov 24, 00:44

**Background**: GPT-6.2 is OpenAI's large language model family, released in two variants: Astra, the heavier high-capability tier, and Sol, a cheaper model positioned for complex coding, computer use and professional work. ChatGPT's Chat tab is the default conversational interface most users see, as opposed to API access or specialized tools. "Proactive suggestions" refers to the assistant volunteering a next action — for example, offering to notify you when a price drops — a step beyond responding only when asked.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-6.2_Sol">GPT-6.2 Sol</a></li>
<li><a href="https://www.cometapi.com/models/openai/gpt-6-2-sol/">GPT 6 . 2 Sol API - Access OpenAI GPT 6 . 2 Sol at Best Price | CometAPI</a></li>

</ul>
</details>

**Tags**: `#ChatGPT`, `#OpenAI`, `#LLM`, `#AI product update`, `#unverified`

---

<a id="item-6"></a>
## [Anthropic says internal Claude model proved VP ≠ VNP, with Lean 4 formalization](https://github.com/anthropics/formal-math/blob/main/vp-vnp/README.md) ⭐️ 8.0/10

On November 24, Anthropic published a paper titled "VP ≠ VNP over every field" together with a Lean 4 formalization, claiming the result was discovered by an internal research Claude model and that both the paper and the code were written by AI. The paper derives a superpolynomial arithmetic-circuit lower bound for the Hamiltonian-cycle polynomial and concludes that VP is a strict subset of VNP. If it holds up, this settles Valiant's 1979 algebraic complexity conjecture, which is the algebraic analogue of P versus NP and has been open for 47 years, and it would be one of the first cases of an AI system producing a genuinely new major theorem rather than merely assisting a human. It would also put formal verification, through Lean 4, at the center of how such claims are adjudicated. The repository reports an audit against three standard axioms and a cross-check by the independent nanoda kernel, with no 'sorry' outside reserved placeholder files, but no human mathematician has yet read the proof, and Lean alone cannot confirm that the formalized statement matches the claimed theorem; Appendix Q reportedly lists discrepancies that still need independent review. The result concerns arithmetic circuits only and says nothing directly about P versus NP.

telegram · zaihuapd · Nov 24, 06:02

**Background**: VP and VNP are algebraic complexity classes introduced by Leslie Valiant in 1979: VP is roughly the set of polynomials computable by polynomial-size arithmetic circuits (the determinant is the canonical example), while VNP is the algebraic analogue of NP (the permanent is the canonical example). Just as P versus NP asks whether easy-to-check problems are easy to solve, VP versus VNP asks whether easily definable polynomials are easy to compute with arithmetic circuits. Lean 4 is a dependently typed proof assistant whose proofs are checked by a small trusted kernel, and 'sorry' is a placeholder that lets a proof admit an unproven step, so a sorry-free development is the basic bar for a complete formalization.

<details><summary>References</summary>
<ul>
<li><a href="https://interestingengineering.com/ai-robotics/claude-proves-vp-not-vnp-valiant-conjecture">Claude claims to prove VP VNP in Valiant 's 47-year-old conjecture</a></li>
<li><a href="https://cstheory.stackexchange.com/questions/529/does-vp-neq-vnp-imply-p-neq-np">cc. complexity theory - Does $ VP \neq VNP $ imply $P \neq NP</a></li>
<li><a href="https://math.mit.edu/~drew/grh/">RH Lean proof : verification files</a></li>

</ul>
</details>

**Tags**: `#complexity-theory`, `#formal-verification`, `#Lean 4`, `#AI-for-math`, `#Anthropic`

---