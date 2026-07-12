---
layout: default
title: "Horizon Summary: 2026-07-12 (ZH)"
date: 2026-07-12
lang: zh
---

> 从 28 条内容中筛选出 7 条重要资讯。

---

1. [人形机器人完成全球首例活猪胆囊手术](#item-1) ⭐️ 10.0/10
2. [vLLM v0.25.0：Model Runner V2 成为默认，PagedAttention 被移除](#item-2) ⭐️ 8.0/10
3. [Nvidia、CoreWeave、Nebius 之间的循环融资分析](#item-3) ⭐️ 8.0/10
4. [推荐在 SQLite 中使用严格表](#item-4) ⭐️ 8.0/10
5. [苹果起诉 OpenAI 窃取商业机密推进硬件业务](#item-5) ⭐️ 8.0/10
6. [U-Boot 引导程序漏洞可导致启动时恶意代码执行](#item-6) ⭐️ 8.0/10
7. [上海计划 2027 年前实现高质量脑机接口](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [人形机器人完成全球首例活猪胆囊手术](https://arstechnica.com/ai/2026/07/humanoid-robots-controlled-by-surgeons-did-world-first-operation-on-live-pigs/) ⭐️ 10.0/10

外科医生远程操控宇树 G1 人形机器人，在活猪身上成功完成两例微创胆囊切除手术，这是通用人形机器人首次用于活体手术。该临床前试验结果已发表在《自然》期刊。 这一突破表明，低成本人形机器人可让机器人手术普及化，使其在农村、战场甚至太空等场景变得可负担。G1 基础款售价 13500 美元，远低于达芬奇等专用手术机器人。 宇树 G1 高约 1.5 米，重约 27 公斤，配备灵巧手后约 67000 美元，而专用系统售价 50 万至数百万美元。加州大学圣地亚哥分校的研究人员领导了这项研究，强调了该机器人占地面积小且价格低廉的优势。

telegram · zaihuapd · 7月11日 02:29

**背景**: 人形机器人是模仿人类形态和运动的通用机器，不同于专为手术设计的达芬奇等专用手术机器人。宇树 G1 是一款低成本、灵巧的人形机器人，拥有 23 个自由度、深度相机和 3D 激光雷达，通常用于研究和通用操作。本实验表明人形机器人可通过远程操控适应精准医疗任务，有望扩大手术可及性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.unitree.com/g1/">Humanoid robot G 1 _ Humanoid Robot ... | Unitree Robotics</a></li>

</ul>
</details>

**标签**: `#robotics`, `#medical`, `#surgery`, `#humanoid`, `#AI`

---

<a id="item-2"></a>
## [vLLM v0.25.0：Model Runner V2 成为默认，PagedAttention 被移除](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 8.0/10

vLLM v0.25.0 将 Model Runner V2 (MRv2) 设为所有稠密模型的默认执行路径，移除了传统的 PagedAttention 实现，并使 Transformers 建模后端达到与原生 vLLM 同等的性能。该版本还引入了新模型、流式解析引擎以及针对异构词表的通用推测解码。 此版本标志着 vLLM 架构的重大转变，精简了推理核心并移除了遗留组件，从而简化了维护并提升了性能。增强的 Transformers 后端和新的推测解码能力进一步巩固了 vLLM 作为领先开源 LLM 服务框架的地位。 MRv2 现在支持 EVS、实时嵌入、Mamba 混合模型的前缀缓存以及支持完整 CUDA 图的动态推测解码。在确保 V1/MRv2 后端稳定后移除了 PagedAttention，Transformers 后端获得了 FP8 MoE 支持和 CUDA 图修复。

github · khluu · 7月11日 20:06

**背景**: vLLM 是一个面向大型语言模型的高吞吐量、内存高效的推理引擎，最初基于 PagedAttention 构建。Model Runner V2 (MRv2) 是一个重新设计的执行核心，解决了早期设计限制并提升了模块化和效率。推测解码通过使用草稿模型每步生成多个 token 并并行验证来加速推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM | vLLM Blog</a></li>
<li><a href="https://docs.vllm.ai/en/v0.22.1/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://docs.vllm.ai/en/stable/features/speculative_decoding/dynamic_speculative_decoding/">Dynamic Speculative Decoding - vLLM</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#open-source`, `#AI infrastructure`, `#model serving`

---

<a id="item-3"></a>
## [Nvidia、CoreWeave、Nebius 之间的循环融资分析](https://io-fund.com/ai-stocks/nvidia-coreweave-nebius-circular-financing-gpu-boom) ⭐️ 8.0/10

一篇分析揭示了 Nvidia、CoreWeave 和 Nebius 之间的循环融资——Nvidia 投资于 GPU 云公司，而这些公司又将资金用于购买 Nvidia 的硬件，引发了对可持续性的质疑。 这种循环融资模式与互联网泡沫如出一辙，可能扭曲激励机制，若 AI 需求不及预期则会带来风险。它影响投资者、云服务提供商及整个 AI 生态系统。 Nvidia 对 CoreWeave 的 20 亿美元投资仅占 CoreWeave 2026 年 350 亿美元资本支出的 5.7%，表明循环程度有限。Nebius 的仪表盘显示仅有少量非抢占式 B200 GPU 可用。

hackernews · adletbalzhanov · 7月11日 17:21 · [社区讨论](https://news.ycombinator.com/item?id=48873836)

**背景**: 循环融资指供应商向客户提供资金用于购买其自身产品。在 AI 领域，Nvidia 投资于使用其 GPU 的云公司如 CoreWeave 和 Nebius，这些公司再购买 Nvidia 硬件。这种相互依赖关系可能放大 AI 需求不足时的损失。行业分析师将其与 1990 年代的科技泡沫相提并论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bloomberg.com/graphics/2026-ai-circular-deals/">AI Circular Deals: How Microsoft, OpenAI and Nvidia Keep Paying Each Other</a></li>
<li><a href="https://en.wikipedia.org/wiki/Circular_financing">Circular financing</a></li>
<li><a href="https://am.jpmorgan.com/us/en/asset-management/adv/insights/market-insights/market-updates/on-the-minds-of-investors/does-circularity-in-ai-deals-warn-of-a-bubble/">Does circularity in AI deals warn of a bubble? | J.P. Morgan Asset Management</a></li>

</ul>
</details>

**社区讨论**: 评论观点不一：有人认为 Nvidia 的股权相对于 CoreWeave 总资本支出较小，循环融资并非主要问题；另一些人强调盈利能力取决于利用率和未来需求；少数人警告可能演变为纸牌屋式的崩盘。

**标签**: `#GPU`, `#AI infrastructure`, `#circular financing`, `#Nvidia`, `#cloud computing`

---

<a id="item-4"></a>
## [推荐在 SQLite 中使用严格表](https://evanhahn.com/prefer-strict-tables-in-sqlite/) ⭐️ 8.0/10

Evan Hahn 的文章主张在 SQLite 中使用严格表（STRICT tables）来强制类型安全，Simon Willison 为 sqlite-utils 添加了`--strict`标志，可轻松将非严格表转换为严格模式。 严格表可以防止数据类型错误导致数据库损坏，这对共享数据库尤其重要。采用这种做法能提高数据库可靠性，并在开发早期捕获错误。 严格表要求每一列具有有效类型之一：INT、INTEGER、REAL、TEXT、BLOB 或 ANY，并在插入时强制类型检查，不过 SQLite 仍会进行一些自动类型转换。没有 ALTER TABLE 语句可以将表转换为严格模式；必须通过复制数据重新创建表。

hackernews · ingve · 7月11日 17:33 · [社区讨论](https://news.ycombinator.com/item?id=48873940)

**背景**: 默认情况下，SQLite 使用“类型亲和性”，允许在任何列中存储任何类型，这可能导致数据损坏。严格表于 SQLite 3.37.0（2021 年 11 月）引入，提供了类似其他 SQL 数据库的严格类型强制。SQLite 文档解释了为什么灵活类型是默认设置，但许多开发者提倡将严格表作为最佳实践，以避免微妙的错误。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sqlite.org/stricttables.html">STRICT Tables</a></li>
<li><a href="https://www.sqlitetutorial.net/sqlite-strict-tables/">SQLite Strict Tables</a></li>
<li><a href="https://evanhahn.com/prefer-strict-tables-in-sqlite/">Prefer STRICT tables in SQLite</a></li>

</ul>
</details>

**社区讨论**: Simon Willison 为 sqlite-utils 贡献了`--strict`标志用于转换表。其他评论者讨论了权衡：一些人同意严格表应该是默认设置，而另一些人则指出缺少像 DATE 这样的数据类型。一个指向 SQLite 的“flextypegood”页面的链接解释了为什么严格模式不是默认设置。

**标签**: `#sqlite`, `#database`, `#best-practices`, `#python`, `#tooling`

---

<a id="item-5"></a>
## [苹果起诉 OpenAI 窃取商业机密推进硬件业务](https://www.cnbc.com/2026/07/10/apple-openai-lawsuit-trade-secrets.html) ⭐️ 8.0/10

2026 年 7 月 10 日，苹果在美国加州北区联邦法院起诉 OpenAI、两名前员工及 io Products，指控其系统性窃取与苹果消费硬件设计、制造和供应链相关的商业机密。 这起诉讼凸显了两大科技巨头在 AI 与硬件领域日益激烈的竞争，可能影响行业人才流动和知识产权保护规范。 苹果指控前员工 Chang Liu 离职后下载了数十份硬件文件，OpenAI 硬件负责人 Tang Yew Tan 在离职前将供应商资料发送至个人邮箱，目前有超过 400 名前苹果员工在 OpenAI 工作。

telegram · zaihuapd · 7月11日 03:14

**背景**: 商业机密是指提供竞争优势的保密商业信息。在科技行业，公司通常通过保密协议和内部安全措施保护设计、工艺和供应商关系。此案凸显了员工在竞争对手之间流动时保护专有知识的挑战。

**标签**: `#Apple`, `#OpenAI`, `#lawsuit`, `#trade secrets`, `#hardware`

---

<a id="item-6"></a>
## [U-Boot 引导程序漏洞可导致启动时恶意代码执行](https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/) ⭐️ 8.0/10

固件安全公司 Binarly 披露了 U-Boot 的 FIT 镜像签名验证代码中的 6 个漏洞，其中 2 个可导致任意代码执行，4 个可造成设备崩溃。 这些漏洞使攻击者能够在操作系统启动前执行代码，绕过安全措施，并可在 BMC 等系统上远程利用，影响大量嵌入式设备和工业系统。 这些漏洞最早可追溯到 U-Boot 2013.07 版本，影响超过 50 个稳定版本及大量下游厂商分支；补丁已被 U-Boot 维护者接受，但需要各硬件厂商集成到固件更新中。

telegram · zaihuapd · 7月11日 08:32

**背景**: U-Boot 是一种广泛使用的嵌入式系统开源引导程序，负责加载操作系统内核。FIT（Flattened Image Tree）镜像通过签名来确保启动过程中的完整性；这些漏洞绕过了该验证。BMC（基板管理控制器）负责管理远程固件更新，尤其容易受到远程利用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.u-boot.org/en/latest/usage/fit/signature.html">U-Boot FIT Signature Verification — Das U-Boot unknown version documentation</a></li>
<li><a href="https://www.binarly.io/">Binarly</a></li>
<li><a href="https://github.com/ARM-software/u-boot/blob/master/common/image-fit.c">u-boot/common/image-fit.c at master · ARM-software/u-boot</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerabilities`, `#U-Boot`, `#bootloader`, `#firmware`

---

<a id="item-7"></a>
## [上海计划 2027 年前实现高质量脑机接口](https://t.me/zaihuapd/42501) ⭐️ 8.0/10

上海市科学技术委员会发布了《上海市脑机接口未来产业培育行动方案（2025-2030 年）》，目标是 2027 年前实现高质量脑控，半侵入式脑机接口产品在国内率先实现临床应用，侵入式脑机接口研发取得突破。 这项政策标志着政府对脑机接口领域的重大投资和战略关注，可能加速临床采用，使上海成为神经工程创新的中心。 该计划要求超过 5 款侵入式和半侵入式脑机接口产品通过医疗器械型式检验和临床试验，旨在恢复失语和瘫痪患者的部分语言和运动功能。

telegram · zaihuapd · 7月11日 15:49

**背景**: 脑机接口（BCI）实现大脑与外部设备的直接通信。半侵入式 BCI（如皮层脑电图 ECoG）将电极放置在大脑表面硬脑膜下，在信号质量与手术风险之间取得平衡。侵入式 BCI 则将电极直接植入脑组织，信号保真度更高但风险也更大。上海的计划针对这两种方法，以推进临床应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Brain–computer_interface">Brain–computer interface - Wikipedia</a></li>
<li><a href="https://www.cell.com/the-innovation/fulltext/S2666-6758(24)00033-X">Fully implantable wireless brain-computer interface for humans: Advancing toward the future: The Innovation</a></li>

</ul>
</details>

**标签**: `#brain-computer interface`, `#neural engineering`, `#China`, `#innovation policy`, `#clinical application`

---