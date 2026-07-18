---
layout: default
title: "Horizon Summary: 2026-07-18 (EN)"
date: 2026-07-18
lang: en
---

> From 35 items, 5 important content pieces were selected

---

1. [Huawei Debuts Ascend 950 SuperNode, Claiming 6.7x NVIDIA's Compute](#item-1) ⭐️ 9.0/10
2. [First Atmosphere Detected on Rocky Exoplanet in Habitable Zone](#item-2) ⭐️ 8.0/10
3. [EU AI Act OpenRAG: 933 legally structured chunks with BGE-M3 embeddings](#item-3) ⭐️ 8.0/10
4. [US lawmakers seek ban on Chinese memory chips in allied supply chains](#item-4) ⭐️ 8.0/10
5. [Meta in Talks to Lease AI Compute to Anthropic in $10B Deal](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Huawei Debuts Ascend 950 SuperNode, Claiming 6.7x NVIDIA's Compute](https://www.ithome.com/0/978/019.htm) ⭐️ 9.0/10

Huawei officially unveiled the Ascend 950 SuperNode (Atlas 950 SuperPoD) at the 2026 World AI Conference, claiming it delivers 6.7 times the total compute power of NVIDIA's NVL144 system with 144 GPUs. The device features 1024 Huawei Ascend processors interconnected via the self-developed UnifiedBus (灵衢) protocol. This announcement marks a significant step in the US-China AI hardware competition, potentially offering a domestic alternative to NVIDIA's high-end systems. If performance claims hold, it could accelerate AI development in China by providing massive compute for training trillion-parameter models. The Ascend 950 SuperNode achieves 1 EFLOPS FP8 and 2 EFLOPS FP4 compute with 256 TB of unified global memory. According to a report by China Securities, it offers 6.7 times the total compute of NVIDIA's 144-card NVL144 system.

telegram · zaihuapd · Jul 17, 10:27

**Background**: Huawei's Ascend series of AI accelerators are designed to compete with NVIDIA's GPUs in the Chinese market, especially under export restrictions. The UnifiedBus (灵衢) protocol is a self-developed interconnect standard that allows scaling up to 8192 processors, replacing PCIe, NVLink, and RDMA. The Atlas 950 SuperPoD is the latest in Huawei's SuperNode line, following the commercial deployment of over 750 Atlas 384 SuperNodes.

<details><summary>References</summary>
<ul>
<li><a href="https://www.huawei.com/cn/news/2026/7/atlas-950-superpod">昇腾950超节点真机亮相2026世界人工智能大会</a></li>
<li><a href="https://locsic.com/zh/thinking/lingqu-unifiedbus-protocol-analysis/">灵衢协议深度分析：中国算力突围的互联赌注 — Locsic</a></li>

</ul>
</details>

**Tags**: `#AI Hardware`, `#Huawei`, `#Ascend`, `#SuperNode`, `#Compute`

---

<a id="item-2"></a>
## [First Atmosphere Detected on Rocky Exoplanet in Habitable Zone](https://www.bbc.com/news/articles/cy4kdd1e0ejo) ⭐️ 8.0/10

Astronomers have detected an atmosphere on LHS 1140b, a super-Earth exoplanet orbiting within the habitable zone of a red dwarf star 48 light-years away, using data from the James Webb Space Telescope. This marks the first confirmed atmosphere on a relatively rocky planet in a habitable zone. This discovery provides a crucial test case for studying potentially habitable exoplanet atmospheres and understanding how rocky planets around red dwarfs retain their atmospheres despite intense stellar radiation. It also narrows the search for biosignatures and advances our ability to characterize Earth-like worlds. LHS 1140b has a mass about 5.6 times Earth's and a radius about 1.7 times larger, giving it a density lower than a purely rocky planet and suggesting it may be an ocean world with 9-19% water by mass. The atmosphere detection came via transmission spectroscopy as the planet transited its star, ruling out a mini-Neptune scenario.

hackernews · neversaydie · Jul 17, 14:06 · [Discussion](https://news.ycombinator.com/item?id=48947560)

**Background**: Exoplanets in the habitable zone—the region where liquid water could exist on a surface—are prime targets for atmospheric study. Red dwarf stars are cooler and smaller than the Sun, making their habitable zones much closer, which exposes planets to strong stellar flares and atmospheric stripping. LHS 1140b was discovered in 2017 by the MEarth Project and has been extensively studied because it transits its star, allowing atmospheric analysis via transit spectroscopy.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cy4kdd1e0ejo">First atmosphere found around Earth-like planet LHS 1140b</a></li>
<li><a href="https://en.wikipedia.org/wiki/LHS_1140_b">LHS 1140 b</a></li>
<li><a href="https://science.nasa.gov/exoplanet-catalog/lhs-1140-b/">LHS 1140 b - NASA Science</a></li>

</ul>
</details>

**Discussion**: Commenters debated whether LHS 1140b qualifies as 'Earth-like,' with some arguing it is more akin to a mini-Neptune being stripped by its star, while others noted that JWST emission spectroscopy rules out a mini-Neptune. Suggestions included building a solar lens telescope for future study and discussions on propulsion to reach the planet within centuries. One comment highlighted the Fermi paradox, noting the narrow time window for civilizations to communicate.

**Tags**: `#exoplanets`, `#astronomy`, `#space exploration`, `#atmospheres`, `#habitability`

---

<a id="item-3"></a>
## [EU AI Act OpenRAG: 933 legally structured chunks with BGE-M3 embeddings](https://www.reddit.com/r/MachineLearning/comments/1uytlac/eu_ai_act_openrag_933_legally_structured_chunks/) ⭐️ 8.0/10

A corpus of the EU AI Act has been released, containing 933 legally structured chunks with BGE-M3 embeddings stored in a single SQLite file, along with evaluation results against a benchmark. This resource enables more accurate retrieval-augmented generation and legal NLP research by respecting the Act's legal structure rather than arbitrary character windows. It provides a reproducible benchmark for evaluating chunking strategies in legal document processing. The corpus chunks per article paragraph, recital, definition, and annex point, with metadata stored separately. It includes exact EUR-Lex links and application-date metadata, and ambiguous cases are left as NULL.

reddit · r/MachineLearning · /u/Automatic-Forever-63 · Jul 17, 08:18

**Background**: Retrieval-augmented generation (RAG) enhances large language models by retrieving relevant information from external sources. BGE-M3 is a versatile embedding model supporting dense, sparse, and multi-vector retrieval. The EU AI Act (Regulation 2024/1689) is a landmark legal framework for artificial intelligence regulation.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/BAAI/bge-m3">BAAI/bge-m3 · Hugging Face</a></li>
<li><a href="https://eur-lex.europa.eu/">EUR - Lex — Access to European Union law — choose your language</a></li>
<li><a href="https://en.wikipedia.org/wiki/Retrieval-augmented_generation">Retrieval-augmented generation - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#EU AI Act`, `#RAG`, `#legal NLP`, `#BGE-M3`, `#SQLite`

---

<a id="item-4"></a>
## [US lawmakers seek ban on Chinese memory chips in allied supply chains](https://www.tomshardware.com/pc-components/dram/lawmakers-want-us-government-to-ban-memory-chips-from-china-even-in-allied-supply-chains-citing-unacceptable-risk-to-national-economic-and-supply-chain-security) ⭐️ 8.0/10

US lawmakers John Moolenaar and George Whitesides have formally requested the Commerce Secretary to block US companies from purchasing memory chips from Chinese manufacturers CXMT and YMTC, and to pressure allies to do the same. This move could reshape global memory supply chains, potentially creating shortages and dependencies that affect AI infrastructure and consumer electronics, and it escalates tech decoupling between the US and China. The letter specifically targets CXMT for inclusion on the Entity List and seeks additional restrictions on YMTC, citing close ties to the Chinese military; companies like Apple are reportedly seeking Chinese memory chips.

telegram · zaihuapd · Jul 17, 14:00

**Background**: Chinese memory chip makers CXMT (DRAM) and YMTC (NAND flash) have emerged as significant players, challenging global leaders like Samsung and SK Hynix. The US has previously imposed export controls on semiconductor technology to China, but this request extends to allied supply chains, indicating a broader strategy to contain China's tech capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-cn/长鑫存储">长 鑫 存 储 - 维基百科，自由的百科全书</a></li>
<li><a href="http://chip.com.cn/ymtc.html">长 江 存 储 ( YMTC ) - Glochip.com</a></li>

</ul>
</details>

**Tags**: `#semiconductor`, `#supply chain`, `#geopolitics`, `#memory chips`, `#AI`

---

<a id="item-5"></a>
## [Meta in Talks to Lease AI Compute to Anthropic in $10B Deal](https://www.nytimes.com/2026/07/17/technology/meta-anthropic-ai-computing-power.html) ⭐️ 8.0/10

Meta is negotiating with AI startup Anthropic to lease its AI data center computing power in a potential two-year deal worth up to $10 billion. This deal highlights the extreme scarcity of AI computing resources and signals a new revenue model for tech giants to monetize their massive infrastructure investments. Anthropic proposed the deal in June 2026; Meta is evaluating it. The arrangement would involve monthly payments with an early exit option for both parties, but negotiations are still early and may not close.

telegram · zaihuapd · Jul 18, 01:14

**Background**: AI compute has become a critical bottleneck as demand for training and inference skyrockets. Meta plans to spend up to $145 billion this year, largely on AI and data centers. Leasing out spare capacity allows Meta to offset costs and generate new revenue.

**Tags**: `#AI compute`, `#Meta`, `#Anthropic`, `#data centers`, `#AI infrastructure`

---