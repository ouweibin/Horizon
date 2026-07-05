---
layout: default
title: "Horizon Summary: 2026-07-05 (ZH)"
date: 2026-07-05
lang: zh
---

> 从 39 条内容中筛选出 15 条重要资讯。

---

1. [20 万美元悬赏全部谷歌图书扫描文件（2025）](#item-1) ⭐️ 9.0/10
2. [利用 AI 评论建议泄露 YouTube 创作者私密视频](#item-2) ⭐️ 9.0/10
3. [LLM 提供商跨用户会话可能泄露](#item-3) ⭐️ 9.0/10
4. [Karpathy 的 nanochat 旨在打造 100 美元的 ChatGPT 克隆](#item-4) ⭐️ 8.0/10
5. [利用 AI 辅助将《命令与征服：将军》原生移植到苹果平台](#item-5) ⭐️ 8.0/10
6. [GPT-5.5 Codex 推理令牌聚类导致性能下降](#item-6) ⭐️ 8.0/10
7. [Linux htop/top 全面指南](#item-7) ⭐️ 8.0/10
8. [更好的模型带来更差的工具调用](#item-8) ⭐️ 8.0/10
9. [USAF：在推理 GPU 上微调 MoE 模型](#item-9) ⭐️ 8.0/10
10. [BaryGraph：每个关系都是独立嵌入文档的知识图谱](#item-10) ⭐️ 8.0/10
11. [华为提出“韬定律”：以时间缩微延长摩尔定律](#item-11) ⭐️ 8.0/10
12. [谷歌禁止 AI 越狱与预测市场扩展](#item-12) ⭐️ 8.0/10
13. [iOS 27 引入 Trust Insights 反诈功能](#item-13) ⭐️ 8.0/10
14. [韩国投资 800 万亿韩元使 DRAM 产量翻倍](#item-14) ⭐️ 8.0/10
15. [香港处理中国过半芯片进口，创历史新高](#item-15) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [20 万美元悬赏全部谷歌图书扫描文件（2025）](https://software.annas-archive.gl/AnnaArchivist/annas-archive/-/work_items/234) ⭐️ 9.0/10

安娜档案（Anna's Archive）宣布一项 20 万美元的悬赏，用于获取谷歌图书（Google Books）的所有扫描文件，旨在让这些作品能够公开访问。 这一悬赏可能极大扩展对数百万本书的开放访问，尤其是那些非公有领域的著作，挑战当前的版权和访问壁垒。它已经引发社区的高度参与和额外的档案捐赠。 该悬赏以工作项形式发布在安娜档案的 GitLab 上，得分 9.0，349 分，表明社区兴趣浓厚。安娜档案聚合来自 Z-Library、Sci-Hub 等影子图书馆的元数据，不直接托管文件。

hackernews · Cider9986 · 7月4日 16:51 · [社区讨论](https://news.ycombinator.com/item?id=48786838)

**背景**: 安娜档案是一个影子图书馆元搜索引擎，于 2022 年启动，旨在将所有书籍编目。谷歌图书已扫描了图书馆中的数百万本书，但由于版权原因，许多书籍仍然无法访问。该悬赏旨在获取整个谷歌图书数据集，以实现不受限制的公共访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anna's_Archive">Anna's Archive</a></li>
<li><a href="https://lib.msu.edu/data/gds">Google Books Dataset | MSU Libraries</a></li>

</ul>
</details>

**社区讨论**: 用户对安娜档案在获取稀有书籍方面所起的作用表示感谢，其中一人分享了找到老旧编程 CD 的个人故事。其他人提到了 SourceLibrary.org 等替代档案，以及对未来互联网爬取挑战的担忧。

**标签**: `#digital libraries`, `#book scanning`, `#open access`, `#archiving`, `#bounty`

---

<a id="item-2"></a>
## [利用 AI 评论建议泄露 YouTube 创作者私密视频](https://javoriuski.com/post/youtube) ⭐️ 9.0/10

YouTube 工作室的 AI 评论建议中存在提示注入漏洞，攻击者可以编写恶意评论，当创作者点击建议的提示时，会泄露私密视频的标题和详细信息。 此漏洞可能泄露创作者未发布或私密内容，破坏对 YouTube 平台的信任，并突显 AI 功能中的系统性安全缺陷。 该攻击利用 AI 模型无法区分开发者定义的提示和用户评论内容，导致执行注入的指令，从而请求私密视频数据。

hackernews · javxfps · 7月4日 16:45 · [社区讨论](https://news.ycombinator.com/item?id=48786781)

**背景**: 提示注入是一种网络安全利用方式，恶意输入覆盖了 AI 模型的预期行为。在此案例中，攻击者的评论包含指令，当通过 YouTube 工作室的评论建议功能访问时，模型将其解释为合法命令。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection</a></li>

</ul>
</details>

**社区讨论**: 一位前谷歌工程师评论称，由于涉及该功能的原始工程师，分类该漏洞可能很复杂。另一位用户对 YouTube 不将提示注入视为漏洞表示沮丧。有人尝试复现未成功，但回复称注入已成功触发。

**标签**: `#security`, `#vulnerability`, `#YouTube`, `#prompt injection`, `#bug bounty`

---

<a id="item-3"></a>
## [LLM 提供商跨用户会话可能泄露](https://github.com/anthropics/claude-code/issues/74066) ⭐️ 9.0/10

多位用户报告在主要 LLM 提供商（Anthropic、OpenAI、Google）中出现潜在的会话或缓存泄漏，响应在不同用户账户之间交换，不相关会话的上下文出现在他们的交互中。 这可能表明多租户 LLM 基础设施中存在严重的安全和隐私漏洞，可能导致敏感数据（如个人对话或商业机密）跨用户账户泄露，影响数百万用户和这些平台的信任。 原帖提到一家提供商的事后分析显示，API 网关出现差一错误导致响应交换；另一用户在 Gemini 中研究无关主题时看到数学辅导回复，暗示存在缓存冲突。

hackernews · chatmasta · 7月4日 14:03 · [社区讨论](https://news.ycombinator.com/item?id=48785485)

**背景**: 大型语言模型通常部署在多租户环境中，共享基础设施（如 KV 缓存）可提高性能，但存在信息意外泄露的风险。学术研究（例如关于选择性 KV 缓存共享以减轻时序侧信道的论文）强调了这些风险。上下文泄漏（即模型输出无意中泄露来自其他会话或训练数据的信息）是 LLM 安全中已知的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2508.08438v1">Selective KV- Cache Sharing to Mitigate Timing Side-Channels in LLM ...</a></li>
<li><a href="https://arxiv.org/abs/2512.16059">[2512.16059] ContextLeak: Auditing Leakage in Private In-Context Learning Methods</a></li>
<li><a href="https://www.cobalt.io/blog/llm-data-leakage-10-best-practices">LLM Data Leakage : 10 Best Practices for Securing LLMs | Cobalt</a></li>

</ul>
</details>

**社区讨论**: 评论中包括多位用户的传闻证据支持此问题，但有些人认为是幻觉或上下文窗口过大所致。Claude Code 团队的 Thariq 承认了该报告，称他们认为这是幻觉，但正在调查。一位用户开玩笑地建议在 AGENTS.md 中添加指令，凸显了怀疑态度。

**标签**: `#security`, `#privacy`, `#LLM`, `#Claude`, `#session-leakage`

---

<a id="item-4"></a>
## [Karpathy 的 nanochat 旨在打造 100 美元的 ChatGPT 克隆](https://github.com/karpathy/nanochat) ⭐️ 8.0/10

Andrej Karpathy 在他的 nanochat 项目中创建了一个分支，旨在仅用 100 美元构建一个类似 ChatGPT 的模型。该项目于 2025 年 10 月 13 日发布，是一个用大约 8000 行 PyTorch 编写的开源大语言模型。 这可能通过大幅降低训练类似 ChatGPT 模型的成本，使强大的 AI 更加普及。如果成功，它将使个人和小型组织能够训练自己的对话式 AI，挑战大型科技公司的主导地位。 nanochat 项目涵盖了从预训练到微调和推理的整个流程，但以最小化形式呈现。它是从头实现的，意味着除了 PyTorch 之外，不依赖现有的较大模型或框架。

github · karpathy · 7月4日 03:44

**背景**: 类似 ChatGPT 的模型通常训练成本高昂，由于巨大的计算和数据需求，往往需要数百万美元。Karpathy 之前的项目 nanoGPT 只关注预训练，而 nanochat 将其扩展为完整的聊天机器人。其目标是用 100 美元的预算实现合理的性能，可能通过使用小模型规模、高效训练技术和有限的数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pypi.org/project/nanochat/">nanochat · PyPI</a></li>
<li><a href="https://www.analyticsvidhya.com/blog/2025/10/andrej-karpathys-nanochat/">Build ChatGPT Clone with Andrej Karpathy's nanochat</a></li>

</ul>
</details>

**标签**: `#AI`, `#ChatGPT`, `#open-source`, `#efficient-models`, `#Karpathy`

---

<a id="item-5"></a>
## [利用 AI 辅助将《命令与征服：将军》原生移植到苹果平台](https://github.com/ammaarreshi/Generals-Mac-iOS-iPad/tree/main) ⭐️ 8.0/10

基于 EA 的 GPL v3 源代码发布，通过 Fable 工具的 AI 辅助转换，实现了《命令与征服：将军》在 macOS、iPhone 和 iPad 上的原生移植。 该移植展示了 AI 辅助代码转换在游戏移植中的实际应用，可能降低将老旧 Windows 游戏引入苹果平台的门槛。同时引发了社区对 AI 生成代码质量和可读性的讨论。 此移植是 fbraz3/GeneralsX 的一个分支，后者完成了 macOS/Linux 移植，而此分支增加了 iOS/iPadOS 支持和引擎修复。它支持触摸控制，如点按选择、拖动框选和双指缩放，并且需要在 Steam 上购买游戏。

hackernews · asronline · 7月4日 19:41 · [社区讨论](https://news.ycombinator.com/item?id=48788283)

**背景**: 《命令与征服：将军》是 EA 于 2003 年发行的即时战略游戏，其源代码于 2021 年以 GPL v3 许可证发布，使社区移植成为可能。AI 辅助转换工具（如 Apple 的 Game Porting Toolkit）利用大语言模型在 API 之间转换代码，加速了移植工作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.apple.com/games/game-porting-toolkit/">Game Porting Toolkit - Games - Apple Developer</a></li>
<li><a href="https://developer.apple.com/videos/play/wwdc2026/357/">Speedrun your game port with agentic coding - WWDC26 - Videos ...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对 AI 辅助移植持积极态度，但指出 AI 生成的文档文本风格令人不适。一些人讨论了类似技术在其他经典 RTS 游戏（如《皇帝：沙丘之战》）上的潜力，另一些人指出了需要 Steam 购买才能运行的设置错误。

**标签**: `#game porting`, `#macOS`, `#iOS`, `#AI-assisted development`, `#open source`

---

<a id="item-6"></a>
## [GPT-5.5 Codex 推理令牌聚类导致性能下降](https://github.com/openai/codex/issues/30364) ⭐️ 8.0/10

用户发现 OpenAI 的 GPT-5.5 Codex 模型存在可复现的性能回退，推理令牌聚类导致复杂任务输出错误。 这一性能回退破坏了用户对 Codex 编码可靠性的信任，而这对依赖 AI 辅助编码的开发者至关重要。同时也凸显了模型一致性的持续挑战，并提醒人们本地模型在稳定性上的优势。 问题表现为模型的推理令牌聚类在间隔约 518 的固定值上（例如 516 个令牌），导致输出错误。当使用 6000-8000 个思考令牌时，模型能返回正确结果，表明存在自适应思维机制的缺陷。

hackernews · maille · 7月4日 21:51 · [社区讨论](https://news.ycombinator.com/item?id=48789428)

**背景**: GPT-5.5 Codex 是 OpenAI 于 2026 年 4 月发布的专用于代码生成的大型语言模型，是 GPT-5.3 Codex 的后续版本，增加了生成文档和电子表格等功能。'推理令牌聚类'指模型的推理输出令牌被人为限制在特定的聚类点上，很可能是自适应思维算法的漏洞所致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=48789428">GPT-5.5 Codex reasoning-token clustering may be leading to degraded performance | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.5">GPT-5.5 - Wikipedia</a></li>
<li><a href="https://openai.com/index/introducing-gpt-5-5/">Introducing GPT‑5.5 - OpenAI</a></li>

</ul>
</details>

**社区讨论**: 用户报告每天都有质量下降，并转向 Claude 等替代方案。一位用户指出模型有时会在恰好 516 个令牌处短路，另一位用户回忆 GPT-5.3 更高效。普遍存在沮丧情绪，呼吁 OpenAI 解决问题。

**标签**: `#GPT-5.5`, `#Codex`, `#performance regression`, `#AI reliability`, `#user experience`

---

<a id="item-7"></a>
## [Linux htop/top 全面指南](https://peteris.rocks/blog/htop/) ⭐️ 8.0/10

一篇 2019 年的博客文章详细解释了 Linux 上 htop 和 top 中每个可见的指标和功能，为系统管理员和开发者提供了参考。 理解 htop 和 top 的指标对于诊断系统性能问题至关重要，而本指南使这些信息对初学者和有经验的用户都易于理解。 文章涵盖了进程状态、CPU 和内存使用、负载平均值以及虚拟内存等不太直观的概念，社区评论推荐 btop 作为现代替代品，并建议禁用用户线程和启用树形视图。

hackernews · theanonymousone · 7月4日 12:00 · [社区讨论](https://news.ycombinator.com/item?id=48784777)

**背景**: htop 和 top 是 Linux 中的命令行系统监控工具，显示进程、资源使用情况和其他系统信息。它们对于性能故障排除至关重要，但由于指标众多可能令人不知所措。本指南帮助用户准确解读这些指标。

**社区讨论**: 评论者对文章的清晰度和深度给予好评，有人推荐 btop 作为更现代的工具。实用技巧包括禁用用户线程以减少杂乱，以及启用树形视图以查看进程层级。

**标签**: `#Linux`, `#htop`, `#system monitoring`, `#command-line tools`, `#reference`

---

<a id="item-8"></a>
## [更好的模型带来更差的工具调用](https://simonwillison.net/2026/Jul/4/better-models-worse-tools/#atom-everything) ⭐️ 8.0/10

Armin Ronacher 发现，较新的 Anthropic Claude 模型（Opus 4.8 和 Sonnet 5）经常生成带有虚构模式键的格式错误的工具调用，而较旧的模型没有表现出这种行为。 这种反直觉的趋势削弱了“更新、更强的模型在工具模式遵循方面更好”的假设，给构建可靠 AI 编码代理和工作流的开发者带来了挑战。 该问题具体出现在 Pi 的 `edits[]` 数组中，其中出现了虚构的键。Armin 认为，针对 Claude Code 内置编辑器的强化学习训练无意中降低了其他自定义工具的性能。

rss · Simon Willison · 7月4日 22:53

**背景**: 工具调用使 LLM 能够通过生成结构化 JSON 参数来调用外部 API 或函数。模式遵循是指精确符合预定义模式的能力。Anthropic 的新 Claude 模型经过强化学习训练，擅长使用 Claude Code 的内置文本编辑器工具，这可能导致它们在与 Pi 的编辑器等其他工具交互时产生虚假键。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/tool-calling">What Is Tool Calling? | IBM</a></li>
<li><a href="https://arxiv.org/html/2502.14905v1">Think Inside the JSON: Reinforcement Strategy for Strict LLM Schema Adherence</a></li>

</ul>
</details>

**标签**: `#AI models`, `#tool use`, `#schema adherence`, `#Claude`, `#LLM reliability`

---

<a id="item-9"></a>
## [USAF：在推理 GPU 上微调 MoE 模型](https://www.reddit.com/r/MachineLearning/comments/1unl62q/if_your_gpu_can_run_inference_it_should_be_able/) ⭐️ 8.0/10

一种名为 USAF 的新型稀疏微调方法允许在用于推理的同一 GPU 上微调混合专家（MoE）模型，已在 AMD RX 6750 XT（12GB 显存）上成功微调 Qwen3-30B-A3B。 这解决了微调大型 MoE 模型通常需要比推理更多内存的关键瓶颈，使许多用户无法进行微调。USAF 通过允许在消费级 GPU 上进行微调，有望加速 MoE 模型的普及。 USAF 仅训练稀疏的专家权重和路由器，避免全模型更新或额外适配器参数。该项目在 Apache 2.0 许可下开源，作者强调不进行商业化。

reddit · r/MachineLearning · /u/tsuyu122 · 7月4日 21:56

**背景**: 混合专家（MoE）模型使用多个专业子网络（专家）和一个路由器来选择每个输入令牌由哪些专家处理。微调这类模型通常需要加载所有专家，导致内存使用远超推理水平。像 USAF 这样的稀疏微调方法旨在仅更新参数子集以减少内存需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://apxml.com/courses/mixture-of-experts-advanced-implementation/chapter-3-training-large-scale-moes/fine-tuning-pretrained-moe">Fine-tuning Strategies for Pre-trained MoE Models</a></li>
<li><a href="https://arxiv.org/html/2504.21190v1">TT-LoRA MoE: Unifying Parameter-Efficient Fine-Tuning and Sparse Mixture-of-Experts</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#fine-tuning`, `#MoE`, `#sparse training`, `#GPU`

---

<a id="item-10"></a>
## [BaryGraph：每个关系都是独立嵌入文档的知识图谱](https://www.reddit.com/r/MachineLearning/comments/1un3lsf/barygraph_knowledge_graph_where_every/) ⭐️ 8.0/10

BaryGraph 提出了一种范式转变，将关系表示为独立的嵌入文档（BaryEdge）而非边，从而能够检索到远距离概念之间的结构桥梁。该项目已在完整的英文维基词典上实现，并提供了预印本和 MCP 服务器。 该方法解决了传统向量搜索和知识图谱的根本局限，即仅将关系视为点之间的邻近性，从而遗漏了跨域连接。它可以通过揭示非显而易见的链接，显著改进检索增强生成（RAG）、语义搜索和科学发现。 该系统存储了约 666 万个源于英文维基词典的文档，使用 nomic-embed-text 嵌入和 MongoDB 进行向量搜索。BaryEdge 通过一个包含连接质量和上下文类型嵌入的公式计算，MetaBary 三元组递归形成树状结构，无需额外的嵌入调用。

reddit · r/MachineLearning · /u/adseipsum · 7月4日 08:24

**背景**: 知识图谱传统上将实体表示为节点，关系表示为边，向量嵌入通常只分配给节点。这意味着遥远概念之间的复杂结构关系常常丢失。BaryGraph 将关系具体化为独立的文档，拥有自己的嵌入，从而可以直接检索并分层组合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/modelcontextprotocol/servers">Model Context Protocol servers - GitHub</a></li>

</ul>
</details>

**标签**: `#knowledge graph`, `#embedding`, `#RAG`, `#semantic search`, `#NLP`

---

<a id="item-11"></a>
## [华为提出“韬定律”：以时间缩微延长摩尔定律](https://t.me/zaihuapd/42346) ⭐️ 8.0/10

在 2026 年上海举行的国际电路与系统研讨会上，华为提出了“韬定律”（τ定律），该定律以时间缩微替代几何缩微，推动半导体性能进步。过去六年，华为已据此设计并量产了 381 款芯片，并计划今年秋季推出采用“逻辑折叠”技术的新麒麟手机芯片。 在摩尔定律逼近物理极限之际，“韬定律”可能为半导体发展提供新路径，无需依赖极端微型化即可持续提升性能。若得到验证，它将增强华为在贸易限制下的芯片能力，并重塑行业对后摩尔时代的扩展策略。 时间缩微方法通过寄生参数降低、逻辑折叠、3D 互连优化和全栈协同调度等技术，在器件、电路、芯片和系统层级减少时间常数τ。华为预计，到 2031 年，基于该定律的芯片晶体管密度可达到 1.4 纳米制程同等水平。逻辑折叠技术通过垂直堆叠芯片层来提升性能和能效。

telegram · zaihuapd · 7月4日 04:56

**背景**: 摩尔定律指出芯片上的晶体管密度大约每两年翻一番，历史上通过几何缩微（缩小特征尺寸）实现，这由 Dennard 缩放定律描述。然而，随着晶体管接近原子尺度，进一步的几何缩微变得极其困难且成本高昂。时间缩微则通过优化系统多层级的时间特性，专注于信号在电路中传播的速度，而不是减小物理尺寸。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Moore's_law">Moore's law - Wikipedia</a></li>
<li><a href="https://d-sci.org/index.php/dsci/article/view/45">Theoretical Research on Time Scaling in Multi-layer Electronic Systems-Exploring Huawei's "Ta (τ) Law" | Digital Science</a></li>
<li><a href="https://www.geeky-gadgets.com/huawei-logic-folding-moores-law/">Huawei Logic Folding: A New Approach to Moore's Law - Geeky ...</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#Huawei`, `#Moore's Law`, `#chip design`, `#technology`

---

<a id="item-12"></a>
## [谷歌禁止 AI 越狱与预测市场扩展](https://developer.chrome.com/blog/cws-policy-updates-2026) ⭐️ 8.0/10

谷歌于 2026 年 7 月 1 日宣布，自 2026 年 8 月 1 日起执行新的 Chrome 网上应用店政策，禁止用于 AI 越狱或预测市场的扩展，并要求数据收集必须严格必要且显著披露。 这一政策更新通过移除整个类别的扩展并收紧数据隐私规则，对 Chrome 扩展开发者产生重大影响，将增强用户对 Chrome 生态系统的安全感和信任。 涉及真实货币交易的预测市场扩展被明确禁止，绕过 AI 服务安全措施的 AI 越狱扩展也被禁止；此外，扩展必须声明所有数据收集行为，若安装后数据处理方式发生变化，须获得用户同意。

telegram · zaihuapd · 7月4日 06:30

**背景**: AI 越狱指绕过 AI 模型（如 ChatGPT）安全限制以生成违规内容的技术。预测市场允许用户用真实货币对未来事件结果下注，类似于赌博。这些做法引发了安全和伦理担忧，促使谷歌更新政策。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://juejin.cn/post/7375791047535099944">给ChatGPT...</a></li>
<li><a href="https://www.gate.com/zh/learn/articles/what-is-a-prediction-market-a-complete-2026-guide-to-the-global-landscape-funding-trends-and-participation-pathways/16901">什么是预测市场？2026 年全球预测市场格局、融资趋势与参与路径全解析...</a></li>

</ul>
</details>

**标签**: `#Chrome`, `#extension`, `#policy`, `#AI`, `#data collection`

---

<a id="item-13"></a>
## [iOS 27 引入 Trust Insights 反诈功能](https://www.cultofmac.com/news/ios-27-trust-insights-feature) ⭐️ 8.0/10

苹果宣布为 iOS 27 推出 Trust Insights 新框架，这是一个设备端反诈功能，通过分析用户行为模式来检测诈骗，同时不访问个人数据。 该功能在保护隐私的同时实时识别诈骗，提升了用户安全性，有望减少苹果生态系统中的金融欺诈。 Trust Insights 通过设备端分析用户交互模式、时机、上下文和传感器数据来检测胁迫行为，仅向服务器发送单一输出值。可关闭但设有冷却期，防止诈骗分子在通话中诱导用户立即关闭。

telegram · zaihuapd · 7月4日 14:30

**背景**: Trust Insights 是在 WWDC 2026 上为 iOS 27、iPadOS 27 和 Mac Catalyst 27 宣布的新框架。它完全在设备端运行，分析打字速度、屏幕导航模式等行为信号，以标记潜在的诈骗行为，例如受害者在电话指导下转账。苹果通过不读取信息、邮件或照片来确保隐私，原始数据在分析后立即丢弃。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ithinkdiff.com/ios-27-trust-insights-scam-detection-framework/">iOS 27 Adds Trust Insights to Detect Scams Before They Happen</a></li>
<li><a href="https://9to5mac.com/2026/07/02/ios-27-helps-apps-detect-when-a-user-may-be-getting-scammed-in-real-time/">iOS 27 helps apps detect when a user may be getting scammed ...</a></li>
<li><a href="https://developer.apple.com/documentation/TrustInsights">Trust Insights | Apple Developer Documentation</a></li>

</ul>
</details>

**标签**: `#iOS`, `#security`, `#anti-fraud`, `#Apple`, `#privacy`

---

<a id="item-14"></a>
## [韩国投资 800 万亿韩元使 DRAM 产量翻倍](https://t.me/zaihuapd/42357) ⭐️ 8.0/10

韩国公布了半导体全国集群计划，将投资 800 万亿韩元，目标是在五年内使 DRAM 产量翻倍，并在西南地区建设四座内存晶圆厂。 这一巨额投资表明韩国决心保持其在全球内存市场的领先地位，而该市场预计五年内将增长四倍，对全球供应链和技术竞争产生影响。 该计划包括 800 万亿韩元的私人投资用于四座内存晶圆厂，以及政府在 15 年内投入 30 万亿韩元用于基础设施和研发。

telegram · zaihuapd · 7月4日 15:15

**背景**: 半导体集群是集中芯片设计、制造和供应链设施的工业区，以提高效率和创新。DRAM（动态随机存取存储器）是一种广泛用于计算机和电子产品的内存芯片。韩国是内存芯片的全球领导者，拥有三星和 SK 海力士等公司。

**标签**: `#semiconductor`, `#DRAM`, `#Korea`, `#investment`, `#manufacturing`

---

<a id="item-15"></a>
## [香港处理中国过半芯片进口，创历史新高](https://thenextweb.com/news/hong-kong-china-ai-chip-trade-hub) ⭐️ 8.0/10

2026 年前五个月，香港经手了中国逾半数的芯片进口，转口至内地的芯片价值约 1240 亿美元，占中国同期芯片采购总额的 52%。 这一变化凸显了香港在地缘政治紧张局势下，作为 AI 相关半导体贸易关键中转枢纽的战略角色，对全球技术供应链以及中国获取先进芯片的渠道具有重要影响。 AI 相关电子产品现已占香港出口的 57%至 70%，香港贸发局因此将 2026 年出口增长预测上调至逾 20%。不过，香港的中间人角色也使其面临中美关系紧张的显著地缘政治风险。

telegram · zaihuapd · 7月5日 02:45

**背景**: 香港的自由港地位（无关税、无资本管制）以及发达的航空货运网络，使其非常适合半导体贸易（高价值、低重量、时效性强）。随着美中在芯片技术上的紧张局势加剧，香港已成为中国进口先进芯片（尤其是用于 AI 应用的芯片）的重要渠道。

**标签**: `#Hong Kong`, `#semiconductor`, `#AI trade`, `#chip imports`, `#geopolitical risk`

---