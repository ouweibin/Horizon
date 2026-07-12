---
layout: default
title: "Horizon Summary: 2026-07-12 (EN)"
date: 2026-07-12
lang: en
---

> From 28 items, 7 important content pieces were selected

---

1. [Humanoid robot performs world's first live pig gallbladder surgery](#item-1) ⭐️ 10.0/10
2. [vLLM v0.25.0: Model Runner V2 Default, PagedAttention Removed](#item-2) ⭐️ 8.0/10
3. [Analysis of Circular Financing Among Nvidia, CoreWeave, Nebius](#item-3) ⭐️ 8.0/10
4. [Prefer strict tables in SQLite](#item-4) ⭐️ 8.0/10
5. [Apple sues OpenAI for trade secret theft in hardware race](#item-5) ⭐️ 8.0/10
6. [U-Boot Bootloader Flaws Allow Firmware Attack at Boot](#item-6) ⭐️ 8.0/10
7. [Shanghai Targets 2027 for High-Quality Brain-Computer Interfaces](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Humanoid robot performs world's first live pig gallbladder surgery](https://arstechnica.com/ai/2026/07/humanoid-robots-controlled-by-surgeons-did-world-first-operation-on-live-pigs/) ⭐️ 10.0/10

Surgeons remotely controlled a Unitree G1 humanoid robot to perform two minimally invasive gallbladder removals on live pigs, a world first for a general-purpose humanoid robot in live surgery. The clinical trial results were published in Nature. This breakthrough demonstrates that low-cost humanoid robots could democratize access to robotic surgery, making it affordable for rural, battlefield, or space settings. At $13,500 base price, the G1 is a fraction of the cost of specialized surgical robots like the da Vinci system. The Unitree G1 is 1.5 meters tall, weighs 27 kg, and costs about $67,000 with a dexterous hand, versus $500,000 to millions for dedicated systems. Researchers from UC San Diego led the study, highlighting the robot's small footprint and affordability.

telegram · zaihuapd · Jul 11, 02:29

**Background**: Humanoid robots are general-purpose machines designed to mimic human form and movement, unlike specialized surgical robots like da Vinci that are built only for surgery. Unitree G1 is a low-cost, dexterous humanoid with 23 degrees of freedom, depth camera, and 3D lidar, typically used for research and general manipulation. This experiment shows humanoid robots can be adapted for precise medical tasks via teleoperation, potentially expanding surgical access.

<details><summary>References</summary>
<ul>
<li><a href="https://www.unitree.com/g1/">Humanoid robot G 1 _ Humanoid Robot ... | Unitree Robotics</a></li>

</ul>
</details>

**Tags**: `#robotics`, `#medical`, `#surgery`, `#humanoid`, `#AI`

---

<a id="item-2"></a>
## [vLLM v0.25.0: Model Runner V2 Default, PagedAttention Removed](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 8.0/10

vLLM v0.25.0 makes Model Runner V2 (MRv2) the default execution path for all dense models, removes the legacy PagedAttention implementation, and achieves performance parity between the Transformers modeling backend and native vLLM. The release also introduces new models, a Streaming Parser Engine, and universal speculative decoding for heterogeneous vocabularies. This release marks a major architectural shift in vLLM, streamlining the inference core and eliminating legacy components, which simplifies maintenance and improves performance. The enhanced Transformers backend and new speculative decoding capabilities further solidify vLLM's position as a leading open-source LLM serving framework. MRv2 now supports EVS, realtime embeddings, prefix caching for Mamba hybrid models, and dynamic speculative decoding with full CUDA graphs. PagedAttention was removed after ensuring V1/MRv2 backends are stable, and the Transformers backend gained FP8 MoE support and CUDA graph fixes.

github · khluu · Jul 11, 20:06

**Background**: vLLM is a high-throughput, memory-efficient inference engine for large language models, originally built around PagedAttention. Model Runner V2 (MRv2) is a redesigned execution core that addresses earlier design limitations and improves modularity and efficiency. Speculative decoding accelerates inference by using a draft model to generate multiple tokens per step, then verifying them in parallel.

<details><summary>References</summary>
<ul>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM | vLLM Blog</a></li>
<li><a href="https://docs.vllm.ai/en/v0.22.1/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://docs.vllm.ai/en/stable/features/speculative_decoding/dynamic_speculative_decoding/">Dynamic Speculative Decoding - vLLM</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#open-source`, `#AI infrastructure`, `#model serving`

---

<a id="item-3"></a>
## [Analysis of Circular Financing Among Nvidia, CoreWeave, Nebius](https://io-fund.com/ai-stocks/nvidia-coreweave-nebius-circular-financing-gpu-boom) ⭐️ 8.0/10

An analysis reveals circular financing among Nvidia, CoreWeave, and Nebius, where Nvidia invests in GPU cloud companies that then spend their capital on Nvidia's hardware, raising questions about sustainability. This circular financing pattern echoes the dot-com bubble and may distort incentives, posing risks if AI demand falters. It affects investors, cloud providers, and the broader AI ecosystem. Nvidia's $2 billion investment in CoreWeave represents only 5.7% of CoreWeave's $35 billion 2026 CapEx, indicating limited circularity. Nebius' dashboard shows only a few non-preemptible B200 GPUs available.

hackernews · adletbalzhanov · Jul 11, 17:21 · [Discussion](https://news.ycombinator.com/item?id=48873836)

**Background**: Circular financing occurs when a vendor lends money to customers to buy its own products. In AI, Nvidia invests in GPU cloud providers like CoreWeave and Nebius, which then purchase Nvidia hardware. This creates interdependencies that could amplify losses if AI demand disappoints. Industry analysts have compared it to the 1990s tech bubble.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bloomberg.com/graphics/2026-ai-circular-deals/">AI Circular Deals: How Microsoft, OpenAI and Nvidia Keep Paying Each Other</a></li>
<li><a href="https://en.wikipedia.org/wiki/Circular_financing">Circular financing</a></li>
<li><a href="https://am.jpmorgan.com/us/en/asset-management/adv/insights/market-insights/market-updates/on-the-minds-of-investors/does-circularity-in-ai-deals-warn-of-a-bubble/">Does circularity in AI deals warn of a bubble? | J.P. Morgan Asset Management</a></li>

</ul>
</details>

**Discussion**: Comments show mixed views: some argue the circular financing is minor given Nvidia's small stake relative to CoreWeave's total CapEx, while others emphasize that profitability depends on utilization and future demand. A few caution that it could collapse into a house of cards.

**Tags**: `#GPU`, `#AI infrastructure`, `#circular financing`, `#Nvidia`, `#cloud computing`

---

<a id="item-4"></a>
## [Prefer strict tables in SQLite](https://evanhahn.com/prefer-strict-tables-in-sqlite/) ⭐️ 8.0/10

Evan Hahn's article argues for using STRICT tables in SQLite to enforce type safety, and Simon Willison added a `--strict` flag to sqlite-utils to easily convert non-strict tables to strict mode. Strict tables prevent data type errors that can corrupt databases, which is especially critical for shared databases. Adopting this practice improves database reliability and catches errors early in development. Strict tables require each column to have one of the valid types: INT, INTEGER, REAL, TEXT, BLOB, or ANY, and enforce type checking on inserts, though SQLite still performs some automatic type conversions. There is no ALTER TABLE to make a table strict; you must recreate it by copying data.

hackernews · ingve · Jul 11, 17:33 · [Discussion](https://news.ycombinator.com/item?id=48873940)

**Background**: By default, SQLite uses 'type affinity' and allows storing any type in any column, which can lead to data corruption. Strict tables, introduced in SQLite 3.37.0 (November 2021), provide rigid type enforcement similar to other SQL databases. The SQLite documentation explains why flexible typing is the default, but many developers advocate for strict tables as a best practice to avoid subtle bugs.

<details><summary>References</summary>
<ul>
<li><a href="https://sqlite.org/stricttables.html">STRICT Tables</a></li>
<li><a href="https://www.sqlitetutorial.net/sqlite-strict-tables/">SQLite Strict Tables</a></li>
<li><a href="https://evanhahn.com/prefer-strict-tables-in-sqlite/">Prefer STRICT tables in SQLite</a></li>

</ul>
</details>

**Discussion**: Simon Willison contributed a `--strict` flag to sqlite-utils for transforming tables. Other commenters debated trade-offs: some agreed strict should be the default, while others noted missing data types like DATE. A link to SQLite's 'flextypegood' page explains why strict mode is not the default.

**Tags**: `#sqlite`, `#database`, `#best-practices`, `#python`, `#tooling`

---

<a id="item-5"></a>
## [Apple sues OpenAI for trade secret theft in hardware race](https://www.cnbc.com/2026/07/10/apple-openai-lawsuit-trade-secrets.html) ⭐️ 8.0/10

On July 10, 2026, Apple filed a lawsuit in the U.S. District Court for the Northern District of California against OpenAI, two former employees, and io Products, alleging systematic theft of trade secrets related to Apple's consumer hardware design, manufacturing, and supply chain. This lawsuit underscores the escalating competition between two tech giants in the AI and hardware space, potentially affecting industry talent mobility and intellectual property protection norms. Apple alleges that former employee Chang Liu downloaded dozens of hardware files after resigning, and that OpenAI hardware head Tang Yew Tan sent supplier data to his personal email before leaving, while over 400 former Apple employees now work at OpenAI.

telegram · zaihuapd · Jul 11, 03:14

**Background**: Trade secrets are confidential business information that provides a competitive advantage. In the tech industry, companies often protect designs, processes, and supplier relationships through nondisclosure agreements and internal security measures. This case highlights the challenges of safeguarding proprietary knowledge when employees move between competitors.

**Tags**: `#Apple`, `#OpenAI`, `#lawsuit`, `#trade secrets`, `#hardware`

---

<a id="item-6"></a>
## [U-Boot Bootloader Flaws Allow Firmware Attack at Boot](https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/) ⭐️ 8.0/10

Firmware security firm Binarly disclosed six vulnerabilities in U-Boot's FIT image signature verification code, with two allowing arbitrary code execution and four causing device crashes. These flaws enable attackers to execute code before the OS boots, bypassing security measures, and can be exploited remotely on systems like BMCs, affecting numerous embedded devices and industrial systems. The vulnerabilities date back to U-Boot version 2013.07 and affect over 50 stable releases and many downstream vendor branches; patches have been accepted by U-Boot maintainers but require vendor integration into firmware updates.

telegram · zaihuapd · Jul 11, 08:32

**Background**: U-Boot is a widely used open-source bootloader for embedded systems, responsible for loading the operating system kernel. FIT (Flattened Image Tree) images are signed to ensure integrity during boot; these vulnerabilities bypass that verification. BMCs (Baseboard Management Controllers) manage remote firmware updates and are especially exposed to remote exploitation.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.u-boot.org/en/latest/usage/fit/signature.html">U-Boot FIT Signature Verification — Das U-Boot unknown version documentation</a></li>
<li><a href="https://www.binarly.io/">Binarly</a></li>
<li><a href="https://github.com/ARM-software/u-boot/blob/master/common/image-fit.c">u-boot/common/image-fit.c at master · ARM-software/u-boot</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerabilities`, `#U-Boot`, `#bootloader`, `#firmware`

---

<a id="item-7"></a>
## [Shanghai Targets 2027 for High-Quality Brain-Computer Interfaces](https://t.me/zaihuapd/42501) ⭐️ 8.0/10

Shanghai's Science and Technology Commission has issued an action plan aiming for high-quality brain control by 2027, with semi-invasive BCI products leading clinical application in China and breakthroughs in invasive BCI research. This policy signals major government investment and strategic focus on BCI, potentially accelerating clinical adoption and positioning Shanghai as a hub for neural engineering innovation. The plan calls for over five invasive and semi-invasive BCI products to pass medical device type testing and clinical trials, aiming to restore partial language and motor functions in patients with aphasia and paralysis.

telegram · zaihuapd · Jul 11, 15:49

**Background**: Brain-computer interfaces (BCIs) enable direct communication between the brain and external devices. Semi-invasive BCIs, such as electrocorticography (ECoG), place electrodes on the brain's surface under the dura, offering a balance between signal quality and surgical risk. Invasive BCIs involve implanting electrodes directly into brain tissue, providing higher signal fidelity but greater risks. Shanghai's plan targets both approaches to advance clinical applications.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Brain–computer_interface">Brain–computer interface - Wikipedia</a></li>
<li><a href="https://www.cell.com/the-innovation/fulltext/S2666-6758(24)00033-X">Fully implantable wireless brain-computer interface for humans: Advancing toward the future: The Innovation</a></li>

</ul>
</details>

**Tags**: `#brain-computer interface`, `#neural engineering`, `#China`, `#innovation policy`, `#clinical application`

---