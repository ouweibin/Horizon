---
layout: default
title: "Horizon Summary: 2026-07-10 (EN)"
date: 2026-07-10
lang: en
---

> From 38 items, 11 important content pieces were selected

---

1. [OpenAI Releases GPT-5.6 with SOTA ARC-AGI-3](#item-1) ⭐️ 9.0/10
2. [TypeScript 7.0 Released with Go Rewrite, Up to 12x Faster](#item-2) ⭐️ 9.0/10
3. [Colibrì Runs GLM 5.2 on 32GB Laptop with Disk Streaming](#item-3) ⭐️ 8.0/10
4. [EU Parliament Greenlights Chat Control 1.0](#item-4) ⭐️ 8.0/10
5. [Postgres rewritten in Rust passes all regression tests](#item-5) ⭐️ 8.0/10
6. [Meta Launches Muse Spark 1.1 with Pricing and Evaluation](#item-6) ⭐️ 8.0/10
7. [Meta Superintelligence 1-Year Progress: Unprecedented Compute and 2000km Interconnects](#item-7) ⭐️ 8.0/10
8. [Ant Open-Sources LingBot-Video: First MoE Embodied Video Model](#item-8) ⭐️ 8.0/10
9. [DJI EV50 Sets Altitude Record Over Everest at 8,861 m](#item-9) ⭐️ 8.0/10
10. [Zhengzhou launches core node of National Supercomputing Internet](#item-10) ⭐️ 8.0/10
11. [OpenAI and US War Dept agree to ban AI domestic surveillance](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Releases GPT-5.6 with SOTA ARC-AGI-3](https://openai.com/index/gpt-5-6/) ⭐️ 9.0/10

OpenAI released GPT-5.6, its latest flagship model available in three sizes (Luna, Terra, Sol), achieving a new state-of-the-art score of 7.8% on the ARC-AGI-3 interactive reasoning benchmark, and introducing improved intent understanding and original image preservation. GPT-5.6 sets a new frontier in AI reasoning and agentic intelligence, surpassing previous models on a benchmark designed to measure human-like interactive reasoning. This release may influence the AI industry's direction toward more autonomous and goal-aware systems that better understand user intent. GPT-5.6 is priced per million tokens as Luna $1/$6, Terra $2.50/$15, Sol $5/$30. The model also includes semantic tips for using intent understanding—developers should specify constraints explicitly while the model infers goals, and the original image dimensions are preserved in image inputs.

hackernews · logickkk1 · Jul 9, 17:04 · [Discussion](https://news.ycombinator.com/item?id=48849066)

**Background**: ARC-AGI-3 is an interactive reasoning benchmark that challenges AI agents to explore novel environments, infer goals, and plan actions—measuring human-like intelligence through turn-based abstract tasks. Intent understanding refers to the AI's ability to infer the user's underlying goal beyond literal wording, improving contextual responses in conversational AI.

<details><summary>References</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://businesslibrary.uflib.ufl.edu/thinking-like-an-ai-intent">AI Intent - Thinking Like an AI: Understanding "Intent" - UF Business Library at University of Florida</a></li>

</ul>
</details>

**Discussion**: Community comments highlighted the developer guide's tips on intent understanding and image preservation, noted high scores on BenchCAD, and confirmed GPT-5.6 Sol's SOTA on ARC-AGI-3. Some users pointed out that Fable 5 was excluded from comparisons due to refusing advanced biology questions, while others debated whether to switch from Claude Code to Codex for coding tasks.

**Tags**: `#AI`, `#GPT-5.6`, `#OpenAI`, `#large language models`, `#benchmarking`

---

<a id="item-2"></a>
## [TypeScript 7.0 Released with Go Rewrite, Up to 12x Faster](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 9.0/10

Microsoft has released TypeScript 7.0, a native version rewritten in Go that achieves 8–12x faster full builds and supports shared-memory multithreading. It can be installed via npm and is supported in editors through the Language Server Protocol (LSP). This release significantly improves developer productivity by reducing build times, which is critical for large codebases. The Go rewrite demonstrates a major shift in compiler implementation strategy, potentially influencing the future of language tooling. New flags --checkers and --builders control parallelism for type-checking and project reference building. A compatibility package allows coexistence with TypeScript 6, but embedded language toolchains like Vue and Svelte still require the older version due to incomplete APIs.

telegram · zaihuapd · Jul 9, 04:01

**Background**: TypeScript is a statically typed superset of JavaScript developed by Microsoft. The previous compiler was written in TypeScript itself, which could become slow for large projects. The Language Server Protocol (LSP) standardizes communication between editors and language servers, enabling code intelligence features.

<details><summary>References</summary>
<ul>
<li><a href="https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/">Announcing TypeScript 7.0 - TypeScript</a></li>
<li><a href="https://en.wikipedia.org/wiki/Language_Server_Protocol">Language Server Protocol - Wikipedia</a></li>
<li><a href="https://devblogs.microsoft.com/typescript/announcing-typescript-7-0-rc/">Announcing TypeScript 7.0 RC - TypeScript</a></li>

</ul>
</details>

**Tags**: `#TypeScript`, `#Go`, `#performance`, `#compiler`, `#Microsoft`

---

<a id="item-3"></a>
## [Colibrì Runs GLM 5.2 on 32GB Laptop with Disk Streaming](https://github.com/JustVugg/colibri) ⭐️ 8.0/10

Developer JustVugg released Colibrì, a lightweight C engine that runs the 744B-parameter GLM 5.2 model on a 32GB RAM laptop using int4 quantization and on-demand disk streaming of MoE experts, achieving 0.1 tokens per second on cold start. This demonstrates that even extremely large MoE models can be run on consumer hardware without a GPU, expanding local AI inference accessibility and sparking community interest in further optimizations. The dense part (~17B params) stays resident in RAM at int4 (~9.9 GB), while 21,504 routed experts (~19 MB each) are stored on disk (~370 GB total) and streamed on demand with a per-layer LRU cache. The engine is a single C file with no runtime dependencies.

hackernews · vforno · Jul 9, 08:05 · [Discussion](https://news.ycombinator.com/item?id=48842459)

**Background**: GLM 5.2 is a Mixture-of-Experts (MoE) large language model with 744B total parameters but only ~40B activated per token. Int4 quantization reduces model size by approximately 4x, enabling larger models to fit in memory. The developer's approach uses disk-based expert streaming and caching to overcome RAM limitations on low-end hardware.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/zai-org/GLM-5.2">zai-org/GLM-5.2 · Hugging Face</a></li>
<li><a href="https://docs.z.ai/guides/llm/glm-5.2">GLM-5.2 - Overview - Z.AI DEVELOPER DOCUMENT</a></li>
<li><a href="https://huggingface.co/docs/transformers/quantization/concept_guide">Quantization concepts · Hugging Face</a></li>

</ul>
</details>

**Discussion**: Community comments are generally positive, praising the engineering effort. Some question practical usability at 0.1 tok/s, while others share similar projects (e.g., Unsloth on Apple Silicon, thinfer for image/video gen). Overall, the sentiment is one of impressed curiosity about the approach.

**Tags**: `#LLM`, `#GLM`, `#local inference`, `#optimization`, `#AI`

---

<a id="item-4"></a>
## [EU Parliament Greenlights Chat Control 1.0](https://www.patrick-breyer.de/en/eu-parliament-greenlights-chat-control-1-0-breyer-our-children-lose-out/) ⭐️ 8.0/10

The European Parliament approved Chat Control 1.0, a measure allowing US tech companies to scan private messages without a warrant until 2028, despite having rejected it twice in March. This sets a dangerous precedent for mass surveillance, undermining privacy and digital rights for hundreds of millions of EU citizens, and raises serious concerns about democratic legitimacy and procedural manipulation. The vote was held under an urgency procedure on the last day before the summer break, requiring an absolute majority of 361 votes to reject; only 314 voted against, so the measure passed by default. Only non-encrypted messages are affected, but critics warn of scope creep.

hackernews · rapnie · Jul 9, 11:03 · [Discussion](https://news.ycombinator.com/item?id=48843923)

**Background**: Chat Control refers to EU proposals to combat child sexual abuse material (CSAM) by scanning private communications. Chat Control 1.0 is a temporary derogation from the ePrivacy Directive that allows platforms to voluntarily scan messages; Chat Control 2.0 is a more permanent regulation still under negotiation. The EU had previously rejected similar scanning mandates in March, but procedural tactics revived 1.0.

<details><summary>References</summary>
<ul>
<li><a href="https://fightchatcontrol.eu/chat-control-overview">Chat Control 1 . 0 vs 2.0 - Fight Chat Control</a></li>
<li><a href="https://overcentral.com/en/eu-parliament-chat-control-revival/">EU Parliament Revives Private Message Scanning Law</a></li>

</ul>
</details>

**Discussion**: Commenters expressed outrage at the parliamentary tactic, noting that the vote was scheduled to minimize opposition and that a majority of voting MEPs opposed the measure. They criticized the erosion of democratic norms and warned that the EU is heading toward totalitarianism.

**Tags**: `#EU policy`, `#privacy`, `#surveillance`, `#chat control`

---

<a id="item-5"></a>
## [Postgres rewritten in Rust passes all regression tests](https://github.com/malisper/pgrust) ⭐️ 8.0/10

The pgrust project, which rewrites PostgreSQL in Rust with LLM assistance, now passes 100% of the Postgres regression tests. The author has been experimenting with LLMs to build a better version of Postgres and is working on a new unpublished version incorporating additional techniques. This achievement demonstrates the potential of using LLMs for large-scale system rewrites, which could lead to a more memory-safe and performant PostgreSQL. It also sparks discussions about the future of database development and the role of AI in systems programming. The project produced 7101 commits in less than a month, all generated by LLMs. The author is now developing a new version that incorporates learned techniques, and the project's license may differ from PostgreSQL's.

hackernews · SweetSoftPillow · Jul 9, 06:18 · [Discussion](https://news.ycombinator.com/item?id=48841676)

**Background**: PostgreSQL is a 30-year-old open-source relational database management system. Rewriting it in Rust, a language known for memory safety and concurrency, could improve security and performance. LLMs (large language models) were used to assist in generating the Rust code, enabling rapid development.

**Discussion**: Comments show a mix of admiration and skepticism. Some praise the use of LLMs and the technical achievement, while others question the project's long-term sustainability, code reviewability, and licensing. The author clarifies the experimental nature and future plans.

**Tags**: `#database`, `#rust`, `#postgresql`, `#llm`, `#software-engineering`

---

<a id="item-6"></a>
## [Meta Launches Muse Spark 1.1 with Pricing and Evaluation](https://ai.meta.com/blog/introducing-muse-spark-meta-model-api/) ⭐️ 8.0/10

Meta has announced Muse Spark 1.1, an agentic AI model with new pricing at $1.25/$4.5 per million tokens and a detailed evaluation report. This release marks Meta's move to monetize agentic AI, potentially lowering costs for developers and intensifying competition with closed-source leaders like OpenAI and Anthropic. The model costs $1.25 per million input tokens and $4.5 per million output tokens, with cached input at $0.15; the evaluation uses a custom harness with 6 CPU cores and 8GB RAM, which a commenter noted violates official Terminal-Bench 2.1 task limits.

hackernews · ot · Jul 9, 14:10 · [Discussion](https://news.ycombinator.com/item?id=48846184)

**Background**: Agentic AI models go beyond simple content generation to perform tasks using tools, multi-agent orchestration, and reasoning. Muse Spark is Meta's first natively multimodal agentic model, supporting text, image, and speech input, with a 262k token context window.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.meta.com/blog/introducing-muse-spark-msl/">Introducing Muse Spark: Scaling Towards Personal Superintelligence</a></li>
<li><a href="https://grokipedia.com/page/Muse_Spark_AI_model">Muse Spark (AI model)</a></li>
<li><a href="https://artificialanalysis.ai/models/muse-spark">Muse Spark - Intelligence, Performance & Price Analysis</a></li>

</ul>
</details>

**Discussion**: The community response includes practical adoption (e.g., simonw created an LLM plugin), critical evaluation feedback (GodelNumbering points out the test harness overrides task limits), and strategic debate (jacobgold suggests Meta should undercut competitors by open-sourcing; alightsoul dismisses closed-source models as irrelevant).

**Tags**: `#Meta`, `#Muse Spark`, `#agentic AI`, `#AI model release`, `#large language models`

---

<a id="item-7"></a>
## [Meta Superintelligence 1-Year Progress: Unprecedented Compute and 2000km Interconnects](https://newsletter.semianalysis.com/p/the-future-of-meta-superintelligence) ⭐️ 8.0/10

Meta Superintelligence Labs has published a one-year progress update detailing the most aggressive compute ramp ever seen, involving 2000km+ interconnects for scale-across supercomputing, and the emergence of a top-tier reinforcement learning environment startup. This update signals Meta's intense push toward superintelligence, potentially outperforming rivals like Google and OpenAI. The scale of infrastructure and novel interconnect technology could define the next generation of AI training capabilities. The compute ramp is described as the most aggressive ever, and the interconnects span over 2000 kilometers. The article also offers strategic advice to Google DeepMind, indicating competitive positioning.

rss · Semianalysis · Jul 9, 19:16

**Background**: Meta Superintelligence Labs was established in mid-2025, focusing on achieving artificial general intelligence and superintelligence. The 'scale-across' approach refers to linking multiple data centers across hundreds of kilometers to form a single supercomputer, which requires ultra-long-distance interconnects.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/the-future-of-meta-superintelligence">The Future of Meta Superintelligence: A 1 Year Progress Update</a></li>
<li><a href="https://en.wikipedia.org/wiki/Meta_Superintelligence_Labs">Meta Superintelligence Labs - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2509.17158v1">ARE: scaling up agent environments and evaluations</a></li>

</ul>
</details>

**Tags**: `#Meta`, `#AI infrastructure`, `#superintelligence`, `#reinforcement learning`, `#compute scaling`

---

<a id="item-8"></a>
## [Ant Open-Sources LingBot-Video: First MoE Embodied Video Model](https://www.qbitai.com/2026/07/446458.html) ⭐️ 8.0/10

Ant Group's LingBot open-sourced LingBot-Video, the world's first MoE-based embodied video foundation model with 30B total parameters and only 3B activated, achieving a state-of-the-art RBench score of 0.620. This model dramatically improves inference efficiency—about 3x faster than comparable dense models—while maintaining high performance, making embodied video generation more accessible for robotics research and applications. LingBot-Video uses a DiT+MoE architecture, a dataset of 70,000 hours of embodied data, and a multi-dimensional reinforcement learning reward system focusing on physical plausibility and task completion. It is released under Apache 2.0 license on GitHub.

telegram · zaihuapd · Jul 9, 04:30

**Background**: Mixture of Experts (MoE) is a machine learning technique where multiple specialized sub-networks (experts) are activated per input via a gating network, enabling larger model capacity with lower computational cost. Diffusion Transformers (DiT) combine diffusion models with transformer architectures for high-quality video generation. Embodied AI focuses on models that can perceive and act in physical environments, such as robots.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://lilianweng.github.io/posts/2024-04-12-diffusion-video/">Diffusion Models for Video Generation | Lil'Log</a></li>

</ul>
</details>

**Tags**: `#MoE`, `#embodied AI`, `#video generation`, `#robotics`, `#open-source`

---

<a id="item-9"></a>
## [DJI EV50 Sets Altitude Record Over Everest at 8,861 m](https://www.163.com/dy/article/L1CUCV940514R9OJ.html) ⭐️ 8.0/10

DJI's unreleased EV50 vertical takeoff and landing (VTOL) cargo drone flew over Mount Everest at 8,861 meters during the 'Peak Mission' scientific expedition, setting a new altitude record for similar drones and collecting atmospheric profile data above 8,000 meters. This achievement demonstrates DJI's advanced drone capabilities in extreme environments, paving the way for high-altitude scientific research and commercial low-altitude logistics such as long-range cargo delivery. The EV50 is a composite-wing VTOL drone that can take off and land vertically, then switch to fixed-wing cruise. During the 12-day mission, it completed 32 sorties with a continuous climb of 3,730 meters and still had 30% battery remaining on return.

telegram · zaihuapd · Jul 9, 06:00

**Background**: VTOL drones combine the flexibility of vertical takeoff and landing with the efficiency of fixed-wing flight, making them ideal for cargo delivery over long distances. The EV50 has a maximum range of 150 km (unloaded) and can carry up to 50 kg. Setting an altitude record near the summit of Mount Everest validates its performance in thin air and extreme cold.

<details><summary>References</summary>
<ul>
<li><a href="https://www.dji.com/cn/ev50">DJI EV 50 - 大疆首款垂直起降运载 无 人 机 - DJI 大疆创新</a></li>

</ul>
</details>

**Tags**: `#drone`, `#DJI`, `#aviation`, `#technology`, `#record`

---

<a id="item-10"></a>
## [Zhengzhou launches core node of National Supercomputing Internet](https://36kr.com/newsflashes/3887797387344387) ⭐️ 8.0/10

On July 9, 2026, the core node of the National Supercomputing Internet was officially launched in Zhengzhou during the Henan Provincial Artificial Intelligence Conference, providing over 100,000 domestic AI computing cards. This node forms the largest single pool of domestic AI computing power on the National Supercomputing Internet platform, significantly boosting China's capability to aggregate and schedule computing resources for AI development. The node is designed to build a nationwide coordinated computing resource scheduling system, taking on core functions such as operations management and resource scheduling, while also integrating supply-demand matching and industry incubation services.

telegram · zaihuapd · Jul 9, 07:00

**Background**: The National Supercomputing Internet is a national project to connect supercomputing centers across China, enabling unified scheduling and sharing of computing resources. It aims to provide high-performance computing power to various sectors, including scientific research and AI development.

**Tags**: `#supercomputing`, `#AI infrastructure`, `#China`, `#computing power`, `#national supercomputer`

---

<a id="item-11"></a>
## [OpenAI and US War Dept agree to ban AI domestic surveillance](https://t.me/zaihuapd/42459) ⭐️ 8.0/10

OpenAI and the US Department of War (formerly the Department of Defense) have agreed in principle to amend their AI cooperation contract to explicitly prohibit the use of AI for domestic surveillance of American citizens. The amendment, proposed by OpenAI CEO Sam Altman, bars intentional surveillance and tracking using personally identifiable information obtained from commercial sources. This policy development sets a precedent for ethical AI use in government contracts, addressing civil liberties concerns and potentially influencing future agreements between AI companies and state actors. It signals growing corporate accountability in preventing mass surveillance technologies from being deployed against citizens. The revised clause specifically prohibits deliberate surveillance of US citizens and prohibits the use of AI to track individuals based on commercially obtained personal identification information. The contract amendment has not yet been finalized, and a similar agreement between Anthropic and the War Department was previously suspended over similar controversies.

telegram · zaihuapd · Jul 9, 13:22

**Background**: The US Department of War was the cabinet department responsible for the US Army from 1789 until it was split into the Department of the Army and the Department of the Air Force in 1947 under the National Security Act. Today's Department of Defense succeeded it. The news refers to the modern Pentagon, using the historical name. AI ethics controversies have intensified as companies like OpenAI and Anthropic engage with military agencies, raising concerns about surveillance and human rights.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/US_Department_of_War">US Department of War</a></li>

</ul>
</details>

**Tags**: `#AI ethics`, `#OpenAI`, `#US government`, `#surveillance`, `#policy`

---