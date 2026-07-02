---
layout: default
title: "Horizon Summary: 2026-07-02 (ZH)"
date: 2026-07-02
lang: zh
---

> 从 39 条内容中筛选出 10 条重要资讯。

---

1. [首个能够生长和分裂的合成细胞诞生](#item-1) ⭐️ 9.0/10
2. [Box3D：由 Box2D 创建者推出的开源 3D 物理引擎](#item-2) ⭐️ 9.0/10
3. [英伟达在 Blackwell 上将 DeepSeek V4 推理成本降至五分之一](#item-3) ⭐️ 9.0/10
4. [索尼将于 2028 年 1 月停止生产实体游戏光盘](#item-4) ⭐️ 8.0/10
5. [Cloudflare 推出基于 HTTP 402 的支付网关](#item-5) ⭐️ 8.0/10
6. [Anthropic 的 Fable 模型回归，安全担忧伴随](#item-6) ⭐️ 8.0/10
7. [arXiv 将于 2026 年成为独立非营利组织](#item-7) ⭐️ 8.0/10
8. [MOTHRAG：无图多跳检索击败基于图的系统](#item-8) ⭐️ 8.0/10
9. [超 140 家企业（含 Visa、Mastercard）联合推出 Open Standard 稳定币网络](#item-9) ⭐️ 8.0/10
10. [Meta 计划出售富余 AI 算力，进军云计算市场](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [首个能够生长和分裂的合成细胞诞生](https://www.quantamagazine.org/for-the-first-time-a-cell-built-from-scratch-grows-and-divides-20260701/) ⭐️ 9.0/10

明尼苏达大学由 Kate Adamala 博士领导的研究团队创造了 SpudCell，这是首个完全由无生命化学物质构建并能生长和分裂的合成细胞。这一突破在 2026 年 7 月 1 日被多个新闻媒体报道，相关手稿已上传至 bioRxiv 预印本服务器。 在合成细胞中实现细胞分裂克服了合成生物学中的一个长期障碍，使研究人员更接近设计定制活细胞，用于医学、生物技术和基础研究。这项工作证明了生命的基本特征可以在实验室中从零开始复制。 SpudCell 通过与'供体脂质体'融合来生长，后者提供脂质、核糖体和其他分子；它使用一种绕过传统细胞骨架的机制进行分裂。该研究因其发表策略引发了一些争议：手稿最初被《细胞》期刊拒绝，随后在 bioRxiv 发布前已与记者分享。

hackernews · defrost · 7月1日 14:20 · [社区讨论](https://news.ycombinator.com/item?id=48747304)

**背景**: SpudCell 是一种由无生命化学物质从零构建的合成细胞，能够进行 DNA 复制、蛋白质合成，以及现在的生长和分裂。以往的合成细胞可以复制 DNA 和摄取营养，但无法分裂——这是一个通常涉及细胞骨架的复杂过程。这项工作是更广泛的合成生物学领域的一部分，该领域旨在构建最小生命形式，以理解生命原理并开发生物技术应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/07/01/science/spud-cell-what-to-know.html">SpudCell : Scientists Made a Cell With Most of the Hallmarks of Life.</a></li>
<li><a href="https://www.biotic.org/research/spudcell/">SpudCell and Biotic — announcement and media factsheet.</a></li>

</ul>
</details>

**社区讨论**: 社区评论既表达了兴奋也带有怀疑。一些评论者讨论了发表过程的争议，指出手稿被《细胞》拒绝，并在同行评审前以保密形式与记者分享。另一些人提出了关于氨基酸手性和蛋白质来源的技术问题，而许多人则赞扬手稿在 bioRxiv 上的公开分享。

**标签**: `#synthetic biology`, `#cell division`, `#breakthrough`, `#biology`, `#research`

---

<a id="item-2"></a>
## [Box3D：由 Box2D 创建者推出的开源 3D 物理引擎](https://box2d.org/posts/2026/06/announcing-box3d/) ⭐️ 9.0/10

Erin Catto 宣布了 Box3D，一个基于 Box2D 传统构建的开源 3D 物理引擎，现已发布在 GitHub 上。该引擎完全用 C 语言实现，并包含一个稳健的软步进刚体求解器。 Box2D 一直是无数独立游戏和强化学习环境的基础；Box3D 填补了开源 3D 物理引擎的空白，可能重塑游戏开发、模拟和机器学习研究。它的发布解决了对现代、维护良好的专有引擎替代品的长期需求。 Box3D 具有原生 C 语言 API、传感器系统和稳健的软步进刚体求解器，但公告未涉及确定性——这对网络游戏很重要。该引擎处于早期阶段，社区渴望了解更多关于确定性基准测试的细节。

hackernews · makepanic · 7月1日 12:12 · [社区讨论](https://news.ycombinator.com/item?id=48745445)

**背景**: Box2D 是 Erin Catto 创建的广泛使用的 2D 物理引擎，为《愤怒的小鸟》等游戏和 OpenAI Gym 中的许多强化学习环境提供支持。其简洁性和性能使其成为开发人员的首选。然而，3D 物理引擎领域缺乏类似的流行开源选项，许多项目依赖专有引擎或较旧的解决方案。Box3D 旨在将 Box2D 的稳健性带入 3D 模拟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/erincatto/box3d">GitHub - erincatto/ box 3 d : Box 3 D is a 3 D physics engine for games</a></li>
<li><a href="https://ziggit.dev/t/box3d-new-3d-physics-engine-with-native-c-api/16452">Box 3 D : new 3 D physics engine with native C API - News - Ziggit</a></li>

</ul>
</details>

**社区讨论**: 社区非常兴奋，评论称赞 Erin Catto 的贡献，并强调 Box2D 对独立游戏和强化学习研究的影响。一些用户询问网络应用的确定性，而另一些用户则警告物理模拟的复杂性以及碰撞检测和求解器中的许多开放问题。

**标签**: `#physics engine`, `#open source`, `#game development`, `#simulation`, `#Erin Catto`

---

<a id="item-3"></a>
## [英伟达在 Blackwell 上将 DeepSeek V4 推理成本降至五分之一](https://blogs.nvidia.com/blog/inference-software-lowest-token-cost/) ⭐️ 9.0/10

英伟达在 Blackwell GPU 上实现了 DeepSeek V4 推理吞吐量 5 倍的提升，将 Token 成本降至五分之一。GB300 上 SGLang 引擎的吞吐量从 4 月的约 2200 Tokens/秒/GPU 提升至 6 月的约 11200 Tokens/秒/GPU。 这一突破大幅降低了大语言模型部署的成本，使 AI 推理对企业而言更具经济可行性。它也展示了推理优化的快速进步，通过额外技术有望实现 20 倍的提升。 该优化利用了内核融合、显存压缩、量化精度路径、改进的内存预算、可中断计算图支持和推理稳定性修复。未来的增强包括分解式服务、新浮点精度和多 Token 预测，有望进一步将吞吐量提升至 20 倍。

telegram · zaihuapd · 7月1日 10:36

**背景**: NVIDIA 的 Blackwell 架构是面向 AI 和高性能计算工作负载的 GPU 平台，是 Hopper 的后续产品。SGLang 是一个开源的、高性能推理引擎，广泛用于大语言模型服务。Token 成本衡量生成每个 Token 所需的费用，是推理效率的关键指标。DeepSeek V4 是一个大语言模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/sgl-project/sglang">GitHub - sgl-project/ sglang : SGLang is a high-performance serving...</a></li>
<li><a href="https://catalogone.com/wp-content/uploads/2024/06/NVIDIA-Blackwell-Technical-Brief.pdf">NVIDIA Blackwell Architecture</a></li>
<li><a href="https://localaimaster.com/blog/sglang-vs-vllm-comparison">SGLang vs vLLM: Complete LLM Inference Engine ... | Local AI Master</a></li>

</ul>
</details>

**标签**: `#NVIDIA`, `#DeepSeek V4`, `#inference optimization`, `#token cost`, `#Blackwell`

---

<a id="item-4"></a>
## [索尼将于 2028 年 1 月停止生产实体游戏光盘](https://blog.playstation.com/2026/07/01/physical-disc-production-ending-in-january-2028-for-new-games-releasing-on-playstation-consoles/) ⭐️ 8.0/10

索尼宣布，新 PlayStation 游戏的实体光盘生产将在 2028 年 1 月前停止，未来游戏将全面转向数字发行。 这标志着游戏行业大规模脱离实体媒体，引发了关于数字所有权、DRM、游戏保存以及消费者权益的担忧。 该公告仅适用于新游戏发行，不涉及现有游戏，且索尼未明确限定版或收藏版光盘是否豁免。此举紧随索尼此前从用户库中移除已购买数字电影的争议事件。

hackernews · Tiberium · 7月1日 12:13 · [社区讨论](https://news.ycombinator.com/item?id=48745456)

**背景**: 实体游戏光盘是数十年来主机游戏的主要载体。索尼 PlayStation 部门通过 PlayStation 商店和订阅服务逐步推动数字销售。停止光盘生产标志着全面转向数字化的未来，与行业趋势一致，但疏远了游戏保存者和实体媒体爱好者。

**社区讨论**: 讨论几乎一边倒地负面，用户引用索尼近期移除已购买电影的事件作为“数字购买即是租赁”的证据。评论者还强调数字版价格高昂、DRM 问题和保存风险，一些人表示将转向 PC 游戏或模拟器。

**标签**: `#gaming`, `#digital ownership`, `#physical media`, `#PlayStation`, `#industry shift`

---

<a id="item-5"></a>
## [Cloudflare 推出基于 HTTP 402 的支付网关](https://blog.cloudflare.com/monetization-gateway/) ⭐️ 8.0/10

Cloudflare 宣布推出一个支付网关，利用 HTTP 402 状态码对其后网络中的任何资源进行收费，实现对 API 调用和机器人访问的微支付。 这可能彻底改变网络货币化方式，让网站运营者直接向 AI 机器人及自动化代理收费，以应对机器人流量成本上升的问题，同时保留对普通用户的免费访问。 该网关基于 x402 协议，这是 Coinbase 开发的开放标准，建立在 HTTP 402 状态码之上；它使用 Solana 上的稳定币进行结算，并与 Cloudflare 现有基础设施集成。

hackernews · soheilpro · 7月1日 13:59 · [社区讨论](https://news.ycombinator.com/item?id=48746914)

**背景**: HTTP 402 状态码自 HTTP/1.1 规范（RFC 7231）起就被保留用于未来数字支付。x402 是一个开放的、原生互联网支付协议，它激活了这一状态码用于微支付，使任何 API 都能在提供内容前要求付款。Cloudflare 庞大的网络使其在推动这一标准采用方面具有独特优势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.x402.org/">x402 - Payment Required | Internet-Native Payments Standard</a></li>
<li><a href="https://solana.com/x402/what-is-x402">What is x402? | Payment Protocol for AI Agents on Solana</a></li>
<li><a href="https://kinsta.com/blog/http-402/">What Is the HTTP 402 Status Code?</a></li>
<li><a href="https://amasty.com/blog/understanding-402-error/">Understanding the 402 Payment Required Error Code</a></li>
<li><a href="https://docs.cdp.coinbase.com/x402/core-concepts/http-402">HTTP 402 - Coinbase Developer Documentation</a></li>

</ul>
</details>

**社区讨论**: 评论者对代理访问的微支付感到兴奋，但也提出了法律和财务复杂性（发票、增值税）的担忧，以及在向机器人收费的同时保留免费人类体验的挑战。一些人认为 Cloudflare 的规模可以克服以往采用失败的困境。

**标签**: `#cloudflare`, `#monetization`, `#microtransactions`, `#web monetization`, `#API`

---

<a id="item-6"></a>
## [Anthropic 的 Fable 模型回归，安全担忧伴随](https://twitter.com/claudeai/status/2072402636813607381) ⭐️ 8.0/10

Anthropic 在停用一段时间后重新推出了 Fable 模型（可能是第 5 版），但社区讨论集中在模型权重泄露风险以及对美国 AI 模型信任的侵蚀上。 这一讨论凸显了 AI 安全社区对前沿模型权重安全的重大担忧，以及对美国 AI 提供商信任丧失可能引发生地缘政治军备竞赛的后果。 评论者指出，Fable 等模型权重可能因意外或恶意行为从数据中心泄露，部分用户认为该模型被过度限制，称其“被拔牙到恶意的程度”。

hackernews · mfiguiere · 7月1日 19:35 · [社区讨论](https://news.ycombinator.com/item?id=48752030)

**背景**: 模型权重是神经网络中的数值参数，决定了模型如何处理输入并生成输出。它们通过训练学习得到，对模型能力至关重要。先进 AI 模型的权重泄露可能使对手滥用该技术，带来安全与安保风险。保护模型权重正成为前沿 AI 公司和政策制定者日益重视的优先事项。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.articsledge.com/post/model-weights">What Are Model Weights and Why Do They Matter in 2026?</a></li>
<li><a href="https://www.engine.is/news/category/ai-essentials-what-are-model-weights">AI Essentials: What are model weights? - ENGINE Background | National Telecommunications and Information ... Securing AI Model Weights: Preventing Theft and Misuse of ... Top Stories Model Parameters in AI: What 70B Really Means (2026) Weights and Bias in Neural Networks - GeeksforGeeks What are weights and biases in AI? - EITCA Academy</a></li>
<li><a href="https://www.rand.org/pubs/research_reports/RRA2849-1.html">Securing AI Model Weights: Preventing Theft and Misuse of ... Top Stories Model Parameters in AI: What 70B Really Means (2026) Weights and Bias in Neural Networks - GeeksforGeeks What are weights and biases in AI? - EITCA Academy</a></li>

</ul>
</details>

**社区讨论**: 社区情绪复杂：一些用户担心权重安全问题及对美国模型缺乏信任，另一些人则认为模型过于受限或多余。有用户指出在 Fable 缺席期间并未想念它，表明其相对于现有替代方案的附加值有限。

**标签**: `#AI safety`, `#model weights`, `#Anthropic`, `#trust`, `#security`

---

<a id="item-7"></a>
## [arXiv 将于 2026 年成为独立非营利组织](https://www.reddit.com/r/MachineLearning/comments/1ukjtlm/on_july_1_2026_arxiv_will_spin_out_from_cornell/) ⭐️ 8.0/10

2026 年 7 月 1 日，arXiv 将脱离其 25 年来的所在地康奈尔大学，成为一个独立的非营利组织，主要资金来自西蒙斯基金会和施密特科学。 这一转变标志着 arXiv（开放获取研究传播的关键平台）的治理和可持续性新模式，可能影响学术交流和基础设施的未来。 此次剥离还伴随着品牌重塑，包括更改网站颜色（放弃红色）。西蒙斯基金会和施密特科学为主要资金支持方。

reddit · r/MachineLearning · /u/Nunki08 · 7月1日 12:07

**背景**: arXiv 是一个科学论文预印本仓库，主要涵盖物理、数学、计算机科学及相关领域。自 1991 年成立以来，一直由康奈尔大学托管和支持。成为独立非营利组织旨在确保长期可持续性和与开放获取使命一致的治理。

**标签**: `#arXiv`, `#open access`, `#research infrastructure`, `#science policy`

---

<a id="item-8"></a>
## [MOTHRAG：无图多跳检索击败基于图的系统](https://www.reddit.com/r/MachineLearning/comments/1ukotww/p_mothretrieval_graphfree_multihop_retrieval_via/) ⭐️ 8.0/10

MOTHRAG 是一个开源的多跳 RAG 框架，它通过使用密集索引和查询时编排，消除了离线构建知识图谱的需求。在 HotpotQA 上达到 78.1% 的准确率，在 2WikiMultiHopQA 上达到 76.3%，在 MuSiQue 上达到 50.5%，超过了 GraphRAG、HippoRAG 和 RAPTOR 等基于图的系统。 这种方法大幅降低了更新频繁变化数据的检索系统的成本和复杂性，使多跳 RAG 适用于动态语料的实际生产环境。它还在无需 GPU 加速的情况下与基于图的系统持平或超越，降低了硬件门槛。 MOTHRAG 的更新只需嵌入并追加，无需重新索引，每次查询成本约 0.03 美元（基于通用 API）。在 MuSiQue 上，它落后于 NeocorRAG（50.5 vs 52.6），表明存在检索召回瓶颈，作者尚未解决。

reddit · r/MachineLearning · /u/Annual-Commercial563 · 7月1日 15:26

**背景**: 多跳检索用于需要跨多个文档推理的复杂问题。传统方案如 GraphRAG 会离线构建知识图谱，当数据变化时更新成本高昂。MOTHRAG 通过使用密集向量索引并在查询时动态编排检索步骤来避免这一问题，类似于多步检索方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pypi.org/project/mothrag/">mothrag · PyPI</a></li>
<li><a href="https://hotpotqa.github.io/">HotpotQA: A Dataset for Diverse, Explainable Multi-hop Question Answering</a></li>
<li><a href="https://www.runlocalai.co/learn/courses/rag-systems-part-2/chapter-12-multi-hop-rag">Multi - Hop RAG — RAG Systems: Part 2 (Chapter 12) | RunLocalAI</a></li>

</ul>
</details>

**标签**: `#RAG`, `#Multi-hop Retrieval`, `#Knowledge Graph`, `#Open Source`, `#Machine Learning`

---

<a id="item-9"></a>
## [超 140 家企业（含 Visa、Mastercard）联合推出 Open Standard 稳定币网络](https://www.reuters.com/business/consortium-including-visa-mastercard-jointly-launch-new-global-stablecoin-2026-06-30/) ⭐️ 8.0/10

2026 年 6 月 30 日，包括 Visa、Mastercard 和 Coinbase 在内的超过 140 家企业联合宣布推出 Open Standard 稳定币网络，并计划于今年晚些时候发行锚定美元的稳定币 Open USD。 该倡议汇集了主要的金融和加密行业参与者，旨在打造开放、低成本、高吞吐量的稳定币支付基础设施，有望推动稳定币在加密货币交易之外的日常支付中的主流采用。 企业可以免费且无限制地铸造和赎回 Open USD，储备收益在扣除管理费后由合作伙伴共享。此次发布正值美国 GENIUS Act 于 2025 年为支付稳定币建立了联邦监管框架之后。

telegram · zaihuapd · 7月1日 11:06

**背景**: 稳定币是锚定美元等稳定资产的加密货币，旨在最小化价格波动。目前，稳定币主要用于加密货币交易，而非主流支付，部分原因是缺乏商业级基础设施和监管清晰度。GENIUS Act 于 2026 年签署成为法律，为美国稳定币监管提供了联邦框架。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://neworleanscitybusiness.com/blog/2026/06/30/visa-mastercard-global-stablecoin-open-usd/">Visa, Mastercard launch global stablecoin ... | New Orleans CityBusiness</a></li>
<li><a href="https://en.wikipedia.org/wiki/GENIUS_Act">GENIUS Act - Wikipedia</a></li>

</ul>
</details>

**标签**: `#stablecoins`, `#payments`, `#Visa`, `#Mastercard`, `#consortia`

---

<a id="item-10"></a>
## [Meta 计划出售富余 AI 算力，进军云计算市场](https://www.bloomberg.com/news/articles/2026-07-02/south-korean-stocks-tumble-6-as-ai-jitters-hurt-chipmakers) ⭐️ 8.0/10

据彭博社 2026 年 7 月 2 日报道，Meta 宣布计划通过其云服务向外部客户出售富余的 AI 算力，这标志着其正式进军云计算市场。该消息叠加苹果洽谈向中国存储芯片厂商采购芯片，导致韩国股市大幅下跌。 此举可能重塑云计算格局，为 AWS、谷歌云和 Azure 增加一个主要竞争对手，并表明大型科技公司可能转变其 AI 基础设施投资的变现方式。韩国市场的反应凸显了投资者对 AI 投入可持续性及 AI 硬件可能过剩的担忧。 彭博报道引用匿名消息来源，而 Meta 历来难以准确预测自身 AI 算力需求，因此是否存在真正的富余产能尚待验证。此外，苹果据称正与两家中国存储芯片厂商洽谈，为面向中国市场的设备采购内存芯片，这引发了对韩国存储巨头三星和 SK 海力士竞争地位的担忧。

telegram · zaihuapd · 7月2日 02:29

**背景**: AI 算力是指训练和运行大型 AI 模型所需的计算能力。Meta、谷歌、微软等科技巨头已投入数十亿美元建设 AI 基础设施，导致三星、SK 海力士等公司的高带宽内存（HBM）芯片需求激增。程序交易是指计算机算法同时执行一篮子股票的大额交易，可能放大市场波动，韩国交易所暂停 Kospi 期货程序化卖出即与此相关。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Program_trading">Program trading</a></li>
<li><a href="https://nightlysolutions.com/trackers-data/meta-to-sell-excess-ai-computing-capacity-via-cloud-business-bloomberg-news-repo-3/">Meta to sell excess AI computing capacity via... - NightlySolutions</a></li>
<li><a href="https://gagadget.com/en/716997-meta-wants-to-sell-its-ai-computing-power-to-the-world-and-take-on-aws-doing-it/">Meta wants to sell its AI computing power to the world — and take on...</a></li>

</ul>
</details>

**标签**: `#Meta`, `#AI computing`, `#cloud computing`, `#industry news`, `#market impact`

---