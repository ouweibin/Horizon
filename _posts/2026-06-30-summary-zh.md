---
layout: default
title: "Horizon Summary: 2026-06-30 (ZH)"
date: 2026-06-30
lang: zh
---

> 从 38 条内容中筛选出 10 条重要资讯。

---

1. [最高法院：地理围栏搜查令需要宪法保护](#item-1) ⭐️ 9.0/10
2. [谷歌代理式 AI 同行评审处理约 1 万篇论文，正式论文发布](#item-2) ⭐️ 9.0/10
3. [三星与 SK 海力士宣布创纪录 AI 投资](#item-3) ⭐️ 9.0/10
4. [vLLM v0.24.0 发布，支持 MiniMax-M3 并优化 DeepSeek-V4](#item-4) ⭐️ 8.0/10
5. [火箭实验室以 80 亿美元收购铱星](#item-5) ⭐️ 8.0/10
6. [WATaBoy：将 Game Boy 指令 JIT 编译到 WebAssembly，性能超越原生解释器](#item-6) ⭐️ 8.0/10
7. [CUDA 内核启动内幕：从代码到 GPU](#item-7) ⭐️ 8.0/10
8. [Ornith-1.0：用于自主编程的自支架 LLM](#item-8) ⭐️ 8.0/10
9. [Cerebras-OpenAI 交易阻碍小型初创公司推理访问](#item-9) ⭐️ 8.0/10
10. [Tesla FSD v14 Lite 将 HW4 级智驾带给 HW3 车辆](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [最高法院：地理围栏搜查令需要宪法保护](https://www.theguardian.com/us-news/2026/jun/29/supreme-court-geofence-warrants-case-decision) ⭐️ 9.0/10

美国最高法院裁定，地理围栏搜查令——即强制谷歌等科技公司交出特定区域内所有设备位置数据的命令——构成第四修正案意义上的搜查，因此需要基于可能理由和特定性的搜查令。 这一里程碑式的裁决显著限制了执法部门在无个别嫌疑的情况下获取批量位置数据的能力，加强了数百万智能手机用户的数字隐私保护，并为类似的监控手段树立了先例。 该案件涉及一起抢劫调查，警方使用地理围栏搜查令获取了案发现场附近 19 个账户的 Google 位置数据；法院判决政府获取较长时间段内的第三方位置数据构成搜查。这一裁决延续了此前 Carpenter 诉美国案（2018 年）保护历史基站位置数据的判决。

hackernews · cdrnsf · 6月29日 15:54 · [社区讨论](https://news.ycombinator.com/item?id=48720924)

**背景**: 地理围栏搜查令是一种逆向搜查令，命令科技公司（如 Google）识别在特定时间段内位于虚拟地理边界（地理围栏）内的所有移动设备。执法部门利用这种搜查令通过筛选大量位置历史数据来识别嫌疑人，实质上是在没有事先个别嫌疑的情况下搜索任何出现在犯罪现场的人。这种做法引发了第四修正案（禁止不合理搜查和扣押）下的宪法担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Geofence_warrant">Geofence warrant</a></li>
<li><a href="https://www.scotusblog.com/2026/06/court-rules-that-law-enforcements-use-of-geofence-warrant-was-a-search/">Court rules that law enforcement’s use of “geofence warrant ...</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了对裁决的支持，但也提出了更广泛的担忧：一位用户指出，尽管监控技术有效，但其易用性存在滥用风险，并与窃听固有的资源限制进行了对比。另一位评论者赞赏法院意见书提供了事实来源，如引用 Riley 诉 California 案。第三位用户举了一个无需手机数据也能识别嫌疑人的例子，强调位置数据并非唯一的监控途径。

**标签**: `#privacy`, `#law`, `#surveillance`, `#Supreme Court`, `#geofence warrant`

---

<a id="item-2"></a>
## [谷歌代理式 AI 同行评审处理约 1 万篇论文，正式论文发布](https://www.reddit.com/r/MachineLearning/comments/1uio9rb/googles_agentic_peerreviewer_handled_10k_papers/) ⭐️ 9.0/10

谷歌在顶级计算机科学会议 ICML 和 STOC 上部署了代理式 AI 同行评审系统，处理了约 1 万篇论文，周转时间仅 30 分钟。正式研究论文显示，该系统比零样本提示（zero-shot prompting）多捕捉 34%的数学错误。 这表明在大型会议上可以实现可扩展的 AI 辅助同行评审，通过提高评审效率和错误检测能力，可能改变科学出版格局。它开创了在会议规模上自动化科学评审的先例。 该系统采用代理式 AI 方法，具备工具使用和多步推理能力，在检测数学错误方面比零样本提示高出 34%。正式论文已发布在 arXiv 上。

reddit · r/MachineLearning · /u/Justgototheeffinmoon · 6月29日 10:05

**背景**: 代理式 AI（agentic AI）指能在既定约束下自主追求目标、使用工具并采取行动的智能体。零样本提示（zero-shot prompting）是一种模型无需任何示例即可执行任务的技术。该工作结合这些概念，自动化了研究论文的同行评审过程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Agentic_AI">Agentic AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zero-shot_prompting">Zero-shot prompting</a></li>

</ul>
</details>

**标签**: `#AI`, `#peer review`, `#machine learning`, `#scientific publishing`

---

<a id="item-3"></a>
## [三星与 SK 海力士宣布创纪录 AI 投资](https://t.me/zaihuapd/42235) ⭐️ 9.0/10

三星计划十年投资 6480 亿美元，SK 海力士计划将产能翻倍并在美国上市，该消息于 6 月 29 日由总统尹锡悦主持的国家简报会上宣布。 这一史无前例的支出凸显了全球 AI 基础设施竞赛，并使韩国成为半导体生产的主导力量，直接影响 AI 硬件的供应和成本。 三星的计划总额为 1000 万亿韩元（6480 亿美元），是韩国历史上最大规模；SK 海力士此前暗示在美国上市筹资 290 亿美元并在五年内产能翻倍，但当天两家公司股价均下跌超 9%，原因与苹果有关。

telegram · zaihuapd · 6月29日 07:00

**背景**: AI 模型需要巨大的计算能力，推动了对 HBM（高带宽内存）和 AI 加速器等先进半导体的需求。“物理 AI”指的是与物理世界交互的 AI 系统，如机器人和自动驾驶汽车，这些系统高度依赖高效芯片。韩国政府积极支持半导体投资，以维持其在全球芯片行业的领先地位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/glossary/generative-physical-ai/">What is Physical AI? | NVIDIA Glossary</a></li>

</ul>
</details>

**标签**: `#AI`, `#semiconductors`, `#Samsung`, `#SK Hynix`, `#investment`

---

<a id="item-4"></a>
## [vLLM v0.24.0 发布，支持 MiniMax-M3 并优化 DeepSeek-V4](https://github.com/vllm-project/vllm/releases/tag/v0.24.0) ⭐️ 8.0/10

vLLM v0.24.0 版本正式发布，新增对 MiniMax-M3 模型的支持，并对 DeepSeek-V4 进行了大量性能优化，包含 571 次提交，来自 256 位贡献者。 作为广泛使用的 LLM 推理引擎，此更新显著扩展了模型兼容性和推理效率，有利于生产环境部署，并惠及广大 AI 开发者社区。 关键改进包括 FlashInfer 稀疏索引缓存将首词时间（TTFT）降低 2-4%，以及预填充块规划优化使端到端吞吐量提升 4%。

github · khluu · 6月29日 19:41

**背景**: vLLM 是一个高性能的大语言模型（LLM）推理引擎，支持多种模型架构和量化格式。首词时间（TTFT）是衡量系统在收到提示后生成第一个输出令牌的速度的关键指标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/flashinfer-ai/flashinfer">GitHub - flashinfer -ai/ flashinfer : FlashInfer : Kernel Library for LLM...</a></li>
<li><a href="https://docs.nvidia.com/nim/benchmarking/llm/latest/metrics.html">Metrics — NVIDIA NIM LLMs Benchmarking</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#release`, `#MiniMax`, `#DeepSeek`

---

<a id="item-5"></a>
## [火箭实验室以 80 亿美元收购铱星](https://investors.rocketlabcorp.com/news-releases/news-release-details/rocket-lab-acquire-iridium-historic-deal-creating-fully) ⭐️ 8.0/10

火箭实验室于 6 月 29 日宣布，将以现金加股票方式收购铱星通信公司，交易总价值约 80 亿美元，每股作价 54 美元。该交易已获双方董事会一致批准，预计将于 2027 年年中完成。 此次收购打造了一家完全整合的太空公司，融合发射、卫星制造和卫星运营能力，类似于 SpaceX 的 Starlink 垂直整合模式。它为火箭实验室提供了稳定的发射客户，并获得了铱星宝贵的 L 波段频谱和全球网络，使其在卫星物联网、直连设备和定位导航授时市场中占据有利地位。 该交易包括为火箭实验室提供 36 亿美元的过桥贷款承诺。铱星拥有超过 255 万活跃订阅者，2025 年营收 8.717 亿美元，EBITDA 利润率达 57%。合并后的实体将瞄准卫星物联网、直连设备和定位导航授时服务等新应用。

hackernews · everfrustrated · 6月29日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=48719485)

**背景**: 火箭实验室是领先的小型卫星发射供应商和航天器制造商，以其 Electron 火箭和正在开发的 Neutron 火箭而闻名。铱星运营着全球最大的商业 L 波段卫星星座，提供全球语音和数据通信。此次收购遵循了航天业垂直整合的趋势，即发射供应商同时拥有卫星网络，如 SpaceX 与 Starlink。

**社区讨论**: 社区评论中，有人担忧随着发射成本下降，太空碎片会增多；另一些人则认为此次收购是保障发射需求的战略举措，类似于 SpaceX 利用 Starlink。有评论指出火箭实验室最初是新西兰公司，但现已转为美国公司；也有人看重获得铱星盈利的卫星业务和频谱的价值。

**标签**: `#acquisition`, `#space industry`, `#rocket lab`, `#iridium`, `#satellite communications`

---

<a id="item-6"></a>
## [WATaBoy：将 Game Boy 指令 JIT 编译到 WebAssembly，性能超越原生解释器](https://humphri.es/blog/WATaBoy/) ⭐️ 8.0/10

一个名为 WATaBoy 的本科项目展示了一款 Game Boy 模拟器，它在运行时使用即时编译将 Game Boy 指令翻译成 WebAssembly 模块，性能超越了传统的原生解释器。 这种方法表明，即时编译到 WebAssembly 可能比原生解释更高效，并为在 iOS 等限制原生 JIT 但允许基于浏览器的 WebAssembly JIT 的平台上实现高性能模拟开辟了可能性。 该模拟器通过动态生成 WebAssembly 模块来实现 JIT：它将 Game Boy 代码的基本块编译成新的 WASM 模块并在运行时链接。基准测试显示，JIT 版本显著优于解释器，不过 Firefox 比 Chrome 和 Safari 慢约 25%。

hackernews · energeticbark · 6月29日 15:02 · [社区讨论](https://news.ycombinator.com/item?id=48720190)

**背景**: Game Boy 模拟器通过解释或重新编译类似 Z80 的指令，在现代硬件上运行老游戏。即时编译在运行时将代码翻译为原生机器码以提高速度。WebAssembly 是一种低层虚拟机，能在浏览器和其他环境中高效运行，并支持通过 V8 和 JavaScriptCore 等引擎进行 JIT 编译。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://humphri.es/blog/WATaBoy/">WATaBoy: JIT-ing Game Boy Instructions to Wasm Beats a Native ...</a></li>
<li><a href="https://github.com/EnergeticBark/WATaBoy">GitHub - EnergeticBark/WATaBoy: A Game Boy emulator with an ...</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞该项目对本科生来说令人印象深刻。有人提到苹果对 iOS 的 JIT 限制，而 WebAssembly JIT 绕过了这些限制。还有人指出 Firefox 性能较慢可能是因为其 WebAssembly 优化器不如 Chrome 激进。此外，也提到了相关工作，如静态重编译 NES 代码和使用 JavaScript 的 eval()实现 JIT。

**标签**: `#JIT`, `#WebAssembly`, `#Game Boy`, `#emulation`, `#performance`

---

<a id="item-7"></a>
## [CUDA 内核启动内幕：从代码到 GPU](https://fergusfinn.com/blog/what-happens-when-you-run-a-gpu-kernel/) ⭐️ 8.0/10

Fergus Finn 发表了一篇详细博客，解释了 CUDA 内核启动的完整过程，从主机端启动命令到 GPU 硬件执行，涵盖了驱动通信、门铃机制和线程束调度。 这篇文章通过将高级 CUDA 语法与底层硬件提交联系起来，填补了 GPU 编程教育中的空白，帮助开发者优化性能并更好地理解 GPU 内部机制。 该文章具体解释了用于向 GPU 提交工作的门铃写入和队列内存描述符（QMD）格式，以及线程束如何在流多处理器上调度。

hackernews · mezark · 6月29日 13:11 · [社区讨论](https://news.ycombinator.com/item?id=48718863)

**背景**: CUDA 内核启动涉及多个层次：用户代码调用内核函数，CUDA 运行时将其转换为命令缓冲区并发送给 GPU 驱动。驱动通过门铃写入等机制通知 GPU 硬件有新任务。在 GPU 内部，任务被组织成线程块，进一步划分为线程束（32 个线程一组）。每个流多处理器上的线程束调度器决定每个周期执行哪个线程束，以隐藏内存延迟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://modal.com/gpu-glossary/device-hardware/warp-scheduler">What is a Warp Scheduler ? | GPU Glossary</a></li>
<li><a href="https://docs.nvidia.com/cuda/cuda-programming-guide/02-basics/writing-cuda-kernels.html">2.3. Writing SIMT Kernels — CUDA Programming Guide</a></li>

</ul>
</details>

**社区讨论**: 评论者赞赏文章的深度，尤其是门铃和 QMD 部分将 CUDA 语法与硬件提交联系起来。一位读者表示在完成 HPC 硕士课程前读到这篇文章会很有帮助。另一位指出 NVIDIA 提供了所引用硬件细节的开放文档。

**标签**: `#CUDA`, `#GPU`, `#kernel launch`, `#HPC`, `#NVIDIA`

---

<a id="item-8"></a>
## [Ornith-1.0：用于自主编程的自支架 LLM](https://simonwillison.net/2026/Jun/29/ornith/#atom-everything) ⭐️ 8.0/10

DeepReinforce 发布了 Ornith-1.0，这是一个新的开源权重 LLM 系列（MIT 许可证），在同类规模的开源模型中达到了最先进的编程基准性能。该系列包括从 9B 到 397B 参数的变体，基于 Gemma 4 和 Qwen 3.5 构建。 此次发布大幅推进了开源权重编程模型，无需外部支架工具即可实现强大的自主编程能力。它通过提供高性能、可本地运行的替代方案，可能加快 AI 辅助软件开发的应用。 该模型系列包括 9B Dense、31B Dense、35B MoE 和 397B MoE 变体，均采用 MIT 许可证。初步测试显示其在自主编程任务上表现强劲，35B GGUF 量化版本通过 LM Studio 本地运行可达 103 tokens/second。

rss · Simon Willison · 6月29日 16:17

**背景**: 自支架 LLM 能够自主生成推理结构（如思维链），无需外部组件，将隐式推理转化为显式文本分解。自主编程（Agentic coding）指使用 AI 代理辅助软件开发任务，如代码生成、调试和测试。Ornith-1.0 基于现有的开源基础模型（Gemma 4 和 Qwen 3.5）构建，开箱即用即可实现强大的编程性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jun/29/ornith/">Ornith-1.0: Self - Scaffolding LLMs for Agentic Coding</a></li>
<li><a href="https://www.lesswrong.com/posts/mAwxebLw3nYbDivmt/scaffolded-llms-less-obvious-concerns">Scaffolded LLMs : Less Obvious Concerns — LessWrong</a></li>
<li><a href="https://en.wikipedia.org/wiki/Agentic_coding">Agentic coding</a></li>

</ul>
</details>

**标签**: `#LLM`, `#open-source`, `#coding`, `#agentic`, `#model`

---

<a id="item-9"></a>
## [Cerebras-OpenAI 交易阻碍小型初创公司推理访问](https://www.reddit.com/r/MachineLearning/comments/1uiqhiv/cerebras_openai_deal_capacity_has_effectively/) ⭐️ 8.0/10

据报道，OpenAI 已同意购买价值约 200 亿美元的 Cerebras 芯片，这实际上将所有近期推理容量分配给了 OpenAI，使 Cerebras 的 API 等待队列对小型初创公司来说变得几乎无限长。 这笔交易凸显了超大规模合作伙伴关系可能垄断新兴 AI 硬件容量，可能扼杀依赖快速 ASIC 推理的小型 AI 初创公司的竞争和创新。 帖子中的初创公司构建实时编码代理，需要持续的高吞吐量推理，每秒 1-2k 个 token，并且有 p95 延迟要求，Cerebras 的晶圆级芯片非常适合，但现在访问被阻止。

reddit · r/MachineLearning · /u/Kortopi-98 · 6月29日 12:00

**背景**: Cerebras Systems 生产 Wafer-Scale Engine (WSE)，这是世界上最大的 AI 处理器，专为快速深度学习推理和训练而设计。小型 AI 初创公司通常依赖这种专用硬件来实现低延迟、高吞吐量的推理，而通用 GPU 可能无法最优地提供。p95 延迟指的是第 95 百分位的响应时间，是实时应用的关键指标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://redis.io/blog/p95-latency/">P95 Latency: What It Is & Why It Matters - Redis</a></li>

</ul>
</details>

**标签**: `#AI`, `#inference`, `#Cerebras`, `#OpenAI`, `#startup`

---

<a id="item-10"></a>
## [Tesla FSD v14 Lite 将 HW4 级智驾带给 HW3 车辆](https://x.com/Tesla_AI/status/2071592820889260101) ⭐️ 8.0/10

Tesla 于 6 月 29 日发布 FSD v14 Lite，通过知识蒸馏和强化学习使 HW3 车辆获得 HW4 级自动驾驶和自动泊车能力。 此次更新将先进的自动驾驶能力扩展到数百万辆较老的 HW3 车辆，展示了 Tesla 通过软件优化和 AI 模型压缩来提升旧硬件的潜力。 新功能包括导航改进、更平滑的变道、减少错误刹车，以及首次支持停车、出库和倒车。速度配置文件现在始终可用。

telegram · zaihuapd · 6月30日 02:26

**背景**: 知识蒸馏将知识从较大的'教师'模型转移到较小的'学生'模型，使 HW3 能够模仿 HW4 的行为。离线强化学习使模型无需实时交互即可从预先收集的数据中学习，加速训练。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation</a></li>
<li><a href="https://arxiv.org/abs/2509.05735">[2509.05735] Offline vs. Online Learning in Model-based RL: Lessons for Data Collection Strategies</a></li>

</ul>
</details>

**标签**: `#Tesla`, `#FSD`, `#autonomous driving`, `#AI`, `#automotive tech`

---