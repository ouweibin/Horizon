---
layout: default
title: "Horizon Summary: 2026-07-09 (ZH)"
date: 2026-07-09
lang: zh
---

> 从 34 条内容中筛选出 14 条重要资讯。

---

1. [TypeScript 7 发布，编译速度提升 8-12 倍](#item-1) ⭐️ 10.0/10
2. [Bun 用 AI 将运行时从 Zig 重写为 Rust](#item-2) ⭐️ 9.0/10
3. [Cloudflare 发布 Meerkat：无需领导者的异步共识算法](#item-3) ⭐️ 9.0/10
4. [约翰迪尔与 FTC 就修理权案和解，农民可自行维修](#item-4) ⭐️ 8.0/10
5. [OpenAI 分析如何提高编码基准测试的完整性](#item-5) ⭐️ 8.0/10
6. [Mistral 推出 Robostral Navigate：无地图机器人导航模型](#item-6) ⭐️ 8.0/10
7. [微软发布 Flint：面向 AI 代理的可视化语言](#item-7) ⭐️ 8.0/10
8. [Grok 4.5 发布：定价有竞争力，声称推理能力更强](#item-8) ⭐️ 8.0/10
9. [FAANG 模拟器引发对科技职业现实的讨论](#item-9) ⭐️ 8.0/10
10. [OpenAI 推出 GPT Live，支持 GPT-5.5 任务委派](#item-10) ⭐️ 8.0/10
11. [Kenton Varda 禁止使用 AI 撰写变更描述](#item-11) ⭐️ 8.0/10
12. [安卓全版本远程 Root 漏洞链曝光](#item-12) ⭐️ 8.0/10
13. [Cloudflare 与 OpenAI 试点用全球网络数据优化 AI 搜索](#item-13) ⭐️ 8.0/10
14. [研究人员通过电磁信号识别手机应用，准确率高达 99%](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [TypeScript 7 发布，编译速度提升 8-12 倍](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 10.0/10

微软宣布了 TypeScript 7.0 的重大发布，与 TypeScript 6 相比，编译速度提升了 8-12 倍，在 VS Code 和 tldraw 等代码库的基准测试中得到了验证。 这一性能突破显著减少了大型 TypeScript 项目的构建时间，提高了开发者的生产力，使 TypeScript 对更大的代码库也更具可行性。 TypeScript 7 基于 Go 语言构建，支持并行解析、类型检查和代码生成。它还引入了显式的并行控制，允许开发者调整性能。

hackernews · DanRosenwasser · 7月8日 16:06 · [社区讨论](https://news.ycombinator.com/item?id=48833715)

**背景**: TypeScript 是 JavaScript 的类型超集，编译为纯 JavaScript。之前的版本使用基于 TypeScript 的编译器，而 TypeScript 7 用 Go 语言重写了编译器，在保持与现有 TypeScript 代码完全兼容的同时实现了大幅提速。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://visualstudiomagazine.com/articles/2026/04/21/typescript-7-0-beta-arrives-on-go-based-foundation-with-10x-speed-claim.aspx">TypeScript 7.0 Beta Arrives on Go-Based Foundation With 10x Speed Claim -- Visual Studio Magazine</a></li>
<li><a href="https://visualstudiomagazine.com/articles/2026/07/08/typescript-7-arrives-to-rock-vs-code-with-go-powered-speed.aspx">TypeScript 7 Arrives to Rock VS Code with Go-Powered Speed -- Visual Studio Magazine</a></li>

</ul>
</details>

**社区讨论**: 社区反应极为积极，评论者称赞团队的工程壮举以及基准测试中展示的惊人速度提升。一些用户开玩笑期待未来的 Rust 重写，而另一些用户则分享了自己移植编译器的经验。

**标签**: `#TypeScript`, `#performance`, `#Microsoft`, `#compiler`, `#programming languages`

---

<a id="item-2"></a>
## [Bun 用 AI 将运行时从 Zig 重写为 Rust](https://bun.com/blog/bun-in-rust) ⭐️ 9.0/10

Bun 团队利用 AI 工具（Fable 和 Claude Code）将整个 JavaScript 运行时从 Zig 重写为 Rust，修复了 3MB 内存泄漏，二进制体积缩小 20%，性能提升 5%。 此次重写展示了大规模 AI 辅助代码迁移的可行性，为广泛使用的 JavaScript 运行时带来了显著的稳定性和性能提升。同时也引发了关于语言选择和社区信任的讨论。 重写由一名工程师使用 Fable（Bun 内部 LLM 工具）和 Claude Code 完成，完成了一个团队需要一年的工作，仅耗时数月。新的 Rust 版本还放弃了对之前 Zig 版本的 LTS 支持，迫使用户迁移。

hackernews · afturner · 7月8日 21:49 · [社区讨论](https://news.ycombinator.com/item?id=48837877)

**背景**: Bun 是一个 JavaScript 运行时，集成了打包器、任务运行器和包管理器，旨在替代 Node.js。它最初用 Zig 编写（一种底层系统语言），但面临内存泄漏和稳定性问题。Rust 是一种内存安全的语言，具有零成本抽象，非常适合性能关键型应用。此次重写利用大语言模型进行代码转换，并由人工监督确保正确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bun_(software)">Bun (software) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>
<li><a href="https://bun.com/">Bun — A fast all-in-one JavaScript runtime</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了复杂情绪：有人称赞了严谨的 AI 辅助流程和 Rust 的安全保障，也有人批评放弃了 Zig 版本且缺乏 LTS 支持。一个显著观点是，重写的成功无意中反映了 Zig 的可靠性问题。

**标签**: `#Bun`, `#Rust`, `#Zig`, `#JavaScript runtime`, `#AI-assisted development`

---

<a id="item-3"></a>
## [Cloudflare 发布 Meerkat：无需领导者的异步共识算法](https://blog.cloudflare.com/meerkat-introduction/) ⭐️ 9.0/10

Cloudflare 推出了 Meerkat，一种无需领导者的异步共识算法，并声称这是 QuePaxa 协议的首个生产实现。 Meerkat 克服了 Raft 等基于领导者的协议在全局分布式系统中的局限性，提供了针对网络不稳定的弹性。这可能会影响未来的分布式数据库和协调服务设计。 Meerkat 消除了对领导者的需求，减少了领导者选举和摇摆带来的开销。与部分同步算法不同，它异步运行，即使在消息延迟高度变化的情况下也能取得进展。

hackernews · bobnamob · 7月8日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=48831565)

**背景**: 共识算法确保分布式系统中的多个节点对单个值达成一致。Paxos 和 Raft 等传统算法是部分同步的，假设网络延迟有界。异步共识可以处理任意延迟，长期以来被认为在理论上可行但实际中不实用。Meerkat 实现了 QuePaxa 这种异步协议，标志着它首次在现实系统中部署。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.geeksforgeeks.org/system-design/leaderless-consensus-algorithms/">Leaderless Consensus Algorithms - GeeksforGeeks</a></li>
<li><a href="https://en.wikipedia.org/wiki/Consensus_(computer_science)">Consensus (computer science) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，将 Meerkat 与 Raft 相比具有误导性，因为 Raft 是围绕强领导者设计的。一些人称赞异步方法能处理混乱的网络，而另一些人则对其读取操作的性能开销表示怀疑。总体情绪是谨慎乐观，技术上对权衡存在辩论。

**标签**: `#distributed-systems`, `#consensus`, `#cloudflare`, `#async-consensus`, `#algorithms`

---

<a id="item-4"></a>
## [约翰迪尔与 FTC 就修理权案和解，农民可自行维修](https://apnews.com/article/john-deere-right-to-repair-agriculture-equipment-cb7514ffedb95c130a976af661f2bc02) ⭐️ 8.0/10

联邦贸易委员会（FTC）与五个州同约翰迪尔达成和解，要求该公司允许农民和独立维修店使用与授权经销商相同的软件和工具来修理设备。 这项和解是修理权运动的重要胜利，可能降低农民的维修成本并减少停机时间，同时为其他软件锁定硬件的制造商树立了先例。 约翰迪尔需向五个州共同支付 100 万美元罚款，并接受 10 年的合规监督。该和解不包括对迪尔软件限制的广泛责任豁免。

hackernews · djoldman · 7月8日 23:37 · [社区讨论](https://news.ycombinator.com/item?id=48838876)

**背景**: 现代的约翰迪尔拖拉机包含限制维修仅限授权经销商的软件，需要特殊工具和“载荷文件”进行部件配对。这使农民感到沮丧，他们面临长时间等待和高昂的简单维修费用，从而推动了修理权运动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pirg.org/edfund/resources/john-deere-repair-software/">Service Obstructor: John Deere software restricts farmer repair</a></li>
<li><a href="https://www.npr.org/2025/01/15/nx-s1-5260895/john-deere-ftc-lawsuit-right-to-repair-tractors">John Deere faces U.S. lawsuit over farmers' ability to repair tractors</a></li>

</ul>
</details>

**社区讨论**: 评论者赞扬了活动家 Louis Rossmann 的贡献，并对小额罚款表示怀疑。一些人认为修理权应是一项基本自由，不应受制于协商和解，而另一些人则呼吁将权利扩展到汽车和电动汽车。

**标签**: `#right to repair`, `#FTC`, `#John Deere`, `#consumer rights`, `#policy`

---

<a id="item-5"></a>
## [OpenAI 分析如何提高编码基准测试的完整性](https://openai.com/index/separating-signal-from-noise-coding-evaluations/) ⭐️ 8.0/10

OpenAI 发布了一份分析报告，探讨如何在编码评估中区分信号与噪声，指出基准污染和作弊行为如何扭曲结果。他们强调需要更好的指标和更谨慎的任务设计。 这项分析很重要，因为虚高的基准测试误导了 AI 社区对代码生成真正进展的判断。改进的评估实践将帮助开发者和研究人员对模型能力做出明智决策。 该分析可能指出，像 SWE-Bench 这样的基准测试包含不到 800 个任务，可以通过人工检查去除污染。社区成员还指出，实验室通过修改超时和硬件配置来制造假结果。

hackernews · sk4rekr0w · 7月8日 21:03 · [社区讨论](https://news.ycombinator.com/item?id=48837396)

**背景**: 基准污染是指训练数据包含测试样例，导致模型分数虚高而并无真正改进。像 SWE-Bench 这样的编码评估旨在衡量代码生成能力，但容易通过过拟合或任务操纵而被作弊。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.deeplearning.ai/the-batch/the-problem-with-benchmark-contamination-in-ai/">The Problem with Benchmark Contamination in AI</a></li>
<li><a href="https://arxiv.org/abs/2406.04244">[2406.04244] Benchmark Data Contamination of Large Language Models: A Survey</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为基准作弊现象普遍存在，有人举出具体例子，如 Terminal Bench 2 上的'gpt-5.5 官方提交'。一些人建议纳入效率指标（例如每 API 花费），而另一些人则认为任务缺陷是现实软件开发固有的。

**标签**: `#AI`, `#benchmarking`, `#coding evaluations`, `#OpenAI`, `#machine learning`

---

<a id="item-6"></a>
## [Mistral 推出 Robostral Navigate：无地图机器人导航模型](https://mistral.ai/news/robostral-navigate/) ⭐️ 8.0/10

Mistral AI 发布了 Robostral Navigate，这是一个拥有 80 亿参数的先进机器人导航模型，仅使用单个 RGB 摄像头，无需预先绘制环境地图即可学习遵循自然语言指令。该模型在 R2R-CE 基准测试中取得了最先进的结果，且完全在模拟环境中训练。 这标志着机器人领域向通用、无需地图的导航迈出了重要一步，有可能让机器人在未经预先地图化的陌生室内环境中运行。它可能加速工业自动化、家用机器人和探索等应用，不过该模型目前尚未公开发布。 Robostral Navigate 是一个拥有 80 亿参数的模型，结合了基于指向的导航和强化学习以实现持续改进。它仅依赖单个 RGB 摄像头和自然语言输入，并且完全在模拟环境中训练。

hackernews · ottomengis · 7月8日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=48832212)

**背景**: 传统的机器人导航通常需要预先构建环境地图，如果地图不正确或机器人被移动而不知情，它们就会迷失方向——这被称为“绑架机器人问题”。无地图导航则依赖实时传感器输入和已学习的模型，在无需预先地图的情况下遵循指令。Mistral 的 Robostral Navigate 基于这种方法，使用单个 RGB 摄像头来理解自然语言指令并在陌生的室内空间中导航。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mistral.ai/news/robostral-navigate/">Robostral Navigate: single-camera AI navigation | Mistral AI</a></li>
<li><a href="https://x.com/MistralAI/status/2074856309438980145">Mistral AI on X: "Announcing Robostral Navigate, our first model for embodied navigation: an 8B robotics navigation model that guides robots to autonomously perform tasks specified with natural language. Single RGB camera. State-of-the-art on R2R-CE. https://t.co/UlmUsXNxhX" / X</a></li>

</ul>
</details>

**社区讨论**: 评论者对无地图导航能力表示兴奋，但指出该模型尚未开放。有人强调了“绑架机器人问题”的挑战，并将其与斯坦福大学的 PIGEON 等先前工作进行了比较。其他人则对将该模型集成到爱好者机器人中表示兴趣，例如用于探索围栏线等任务的农场机器人。

**标签**: `#robotics`, `#AI`, `#navigation`, `#Mistral`, `#mapless navigation`

---

<a id="item-7"></a>
## [微软发布 Flint：面向 AI 代理的可视化语言](https://microsoft.github.io/flint-chart/#/) ⭐️ 8.0/10

微软开源了 Flint，这是一种可视化中间语言，允许 AI 代理从简单的高级规范生成高质量图表，无需指定缩放、坐标轴等底层细节。 Flint 解决了 LLM 生成可视化的关键限制：现有的图表语言要么过于简单导致质量低下，要么过于冗长影响代理可靠性。通过提供确定性编译层，Flint 可以使 AI 驱动应用的数据可视化更易用且更可靠。 Flint 使用基于语义类型的规范，并包含布局优化引擎，可自动填充派生出的低级细节。它已支持微软的 Data Formulator，还提供了 MCP 服务器，可轻松集成到现有 AI 代理工作流中。

hackernews · chenglong-hn · 7月8日 17:46 · [社区讨论](https://news.ycombinator.com/item?id=48834924)

**背景**: Flint 是一种可视化中间语言，充当高级人类意图与低级图表渲染之间的桥梁。它与 Vega 或 Matplotlib 等传统图表库不同，传统库需要明确指定每个视觉元素。通过抽象这些细节，Flint 允许 AI 代理专注于数据关系，同时由确定性编译器处理美学和布局优化。

**社区讨论**: 社区讨论呈现不同反应：一些开发者赞赏为代理设计中间语言的想法，而另一些则质疑 Flint 与 Vega 等现有 DSL 的区别。还有争论认为 LLM 是否真的难以处理冗长代码，还是真正的挑战在于空间推理。有评论者表示在自己的工作中并未遇到 Flint 声称要解决的可靠性问题。

**标签**: `#visualization`, `#AI agents`, `#Microsoft`, `#declarative language`, `#LLM`

---

<a id="item-8"></a>
## [Grok 4.5 发布：定价有竞争力，声称推理能力更强](https://x.ai/news/grok-4-5) ⭐️ 8.0/10

xAI 发布了新模型 Grok 4.5，声称推理效率是 Opus 的 4 倍，定价为每百万 token $2/$6，远低于 GPT-5.4 和 Opus 4.8 等竞争模型。 如果基准测试结果属实，Grok 4.5 可能会以低成本提供高性能，从而颠覆 AI 定价格局，迫使竞争对手降价。然而，对 xAI 透明度的持续不信任可能会限制企业采用。 该模型使用了数万亿 token 的 Cursor 数据进行训练，捕获了现实世界中的开发者-代理交互，这可能会使其在代码相关任务中具有优势。定价为每百万输入 token $2，每百万输出 token $6。

hackernews · BoumTAC · 7月8日 18:00 · [社区讨论](https://news.ycombinator.com/item?id=48835111)

**背景**: xAI 由 Elon Musk 于 2023 年创立，开发 Grok 系列 AI 模型。该公司因其内容审核政策和政治偏见指控而面临批评。Grok 4.5 模型在 xAI 网站上公布，并在一篇由提供训练数据的代码编辑器 Cursor 撰写的博客文章中进一步说明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/XAI_(company)">XAI (company)</a></li>
<li><a href="https://grokipedia.com/page/xAI_company">xAI (company)</a></li>

</ul>
</details>

**社区讨论**: 社区评论对 xAI 的可信度表示怀疑，用户担心模型输出的政治导向以及缺乏对 CSAM 的审核。然而，也有人承认该模型具有令人印象深刻的成本效率和基准性能，称其“非常经济”。

**标签**: `#AI`, `#Grok`, `#xAI`, `#machine learning`, `#pricing`

---

<a id="item-9"></a>
## [FAANG 模拟器引发对科技职业现实的讨论](https://www.abeyk.com/escape-the-rat-race/) ⭐️ 8.0/10

一款名为“FAANG 模拟器”的网页职业模拟游戏发布，模拟在 FAANG 等大型科技公司工作的经历，并迅速引发社区对其真实性的讨论。 该模拟器引发许多开发者的共鸣，凸显了年龄歧视、副业压力以及科技行业的拼搏文化等问题。它以创意互动的形式反映职业动态，引发有价值的社区思考。 玩家可以通过住在更便宜的地方或做无法规模化的工作来“破解”游戏。评论建议添加非美国公民模式，其中失业会导致失败，并指出游戏未考虑年龄歧视，同时副业的高成功率被批评为不切实际。

hackernews · nerdbiscuits · 7月8日 20:05 · [社区讨论](https://news.ycombinator.com/item?id=48836778)

**背景**: FAANG 指代主要科技公司：Facebook (Meta)、Apple、Amazon、Netflix 和 Google。该模拟器反映了科技文化，其中员工常面临激烈绩效压力、强制排名以及追求可能被收购的副业。这类模拟允许玩家在无现实后果的情况下探索职业路径。

**社区讨论**: 社区评论既带有幽默也包含批评：有人认为它痛苦地真实，也有人指出缺少年龄歧视等元素以及副业成功率不切实际。建议包括考虑生活成本的地理调整以及为非美国公民添加签证压力模式。

**标签**: `#FAANG`, `#simulation`, `#tech culture`, `#community discussion`

---

<a id="item-10"></a>
## [OpenAI 推出 GPT Live，支持 GPT-5.5 任务委派](https://openai.com/index/introducing-gpt-live/) ⭐️ 8.0/10

OpenAI 推出了 GPT Live 语音模式，该模式可以在后台将任务委派给 GPT-5.5，从而实现实时头脑风暴和长时间对话，无需担心语音模型落后于前沿 AI。 这标志着语音助手向前迈出了重要一步，弥合了语音交互与最强文本模型之间的差距，有望让 AI 对话更高效、更自然。 有用户报告了一个 bug：GPT Live 会打断并在一开始并未预期的时刻发笑；此外，一些用户指出 GPT Live 在语音模式下缺乏工具/连接器支持，限制了生产性任务。

hackernews · logickkk1 · 7月8日 17:03 · [社区讨论](https://news.ycombinator.com/item?id=48834405)

**背景**: GPT Live 是 OpenAI 新推出的语音模式，能够进行连续对话，并将复杂查询委派给更先进的文本模型 GPT-5.5，而不是仅依赖语音优化模型。这种设计旨在在保持对话流畅的同时提供更丰富的回答。

**社区讨论**: 社区反应不一：一些用户称赞长对话能力和委派功能，而另一些则对 AI 取代人际交往表示伦理担忧，并指出语音模式下缺乏工具集成。OpenAI 的一位用户提到 GPT-Live-1 是第一个版本，暗示未来会有改进。

**标签**: `#OpenAI`, `#AI voice assistant`, `#GPT-5.5`, `#ethics`, `#product launch`

---

<a id="item-11"></a>
## [Kenton Varda 禁止使用 AI 撰写变更描述](https://simonwillison.net/2026/Jul/8/kenton-varda/#atom-everything) ⭐️ 8.0/10

知名工程师 Kenton Varda 宣布其团队禁止使用 AI 撰写的变更描述（如 PR 和提交信息），称这些描述遗漏了必要的上下文，在代码审查中比无用更糟。 这位知名工程师的观点凸显了 AI 在软件开发中的一个实际陷阱：AI 生成的信息往往聚焦于低层代码细节，却忽略了高层意图，从而增加了代码审查的难度。它为考虑采用 AI 辅助编程的团队提供了可操作的见解。 Varda 特别批评 AI 描述只罗列 diff 中可见的代码细节，却缺失了理解代码功能所需的整体框架。禁令涵盖 PR 消息、提交信息以及问题/工单描述。

rss · Simon Willison · 7月8日 20:03

**背景**: 变更描述（提交信息、PR 描述）旨在解释为何做出变更，而不仅仅说明变更了什么。好的描述为审查者提供上下文、理由和高层次的理解。LLM 等 AI 工具越来越多地被用于自动生成这些描述，但它们常常产生浅显的摘要，无法捕捉开发者的意图。

**标签**: `#ai-assisted-programming`, `#generative-ai`, `#code review`, `#software engineering`

---

<a id="item-12"></a>
## [安卓全版本远程 Root 漏洞链曝光](https://www.coolapk.com/feed/72700258?s=ZGQ2MTVlZjYxMDYyNTM3ZzZhNGUzOThjega1640) ⭐️ 8.0/10

网络安全公司 Nebula 曝光了一套远程 Root 漏洞链，覆盖所有安卓版本，结合了 Firefox 浏览器漏洞和潜伏 15 年的 Linux 内核漏洞。概念验证代码已在 GitHub 发布。 该漏洞链极为严重，因为只需点击一次即可远程获取任何安卓设备的 Root 权限，可能影响数十亿设备。其中包含一个潜伏 15 年的内核漏洞，揭示了系统性的安全漏洞。 该攻击链利用 Firefox 151.0.2 及更早版本漏洞和一个 Linux 内核漏洞，该内核漏洞近期已被修复。谷歌 Pixel 设备已被证实可被攻破，完整漏洞细节暂未披露以等待补丁部署。

telegram · zaihuapd · 7月8日 13:01

**背景**: 远程 Root 漏洞允许攻击者在没有物理接触设备的情况下获得完全的系统控制权。安卓的安全模型依赖于沙盒和权限机制，但一系列漏洞组合可以绕过这些保护，特别是当浏览器和内核漏洞被结合利用时。

**标签**: `#Android`, `#security`, `#vulnerability`, `#remote root`, `#Linux kernel`

---

<a id="item-13"></a>
## [Cloudflare 与 OpenAI 试点用全球网络数据优化 AI 搜索](https://36kr.com/newsflashes/3886946347694593) ⭐️ 8.0/10

7 月 8 日，Cloudflare 与 OpenAI 宣布启动一项研究试点，利用 Cloudflare 全球网络的实时网站信号（如内容更新鲜度、流量质量、页面变动）来帮助 AI 搜索引擎更高效地发现和索引开放网络内容。 这项合作可能通过基于实际网络活动的近乎实时索引，超越传统的周期性爬取，显著提升 AI 搜索结果的时效性和准确性，有望为 AI 系统获取新鲜信息树立新标准。 该试点旨在利用 Cloudflare 网络中的内容更新频率、页面变动信号和流量质量指标来指导 OpenAI 的搜索索引，而非仅依赖周期性爬取。这种方法可减少新内容出现在 AI 搜索结果中的延迟。

telegram · zaihuapd · 7月8日 15:27

**背景**: 传统网络搜索引擎依赖爬虫定期重新访问网站来更新索引，这可能导致内容陈旧或缺失。Cloudflare 运营着处理大量互联网流量的庞大全球网络，能够实时洞察网站变化和流量模式。通过将 Cloudflare 的实时数据与 OpenAI 的 AI 模型结合，该试点旨在创建一个更灵敏、更准确的搜索索引系统。

**标签**: `#Cloudflare`, `#OpenAI`, `#AI search`, `#web indexing`, `#partnership`

---

<a id="item-14"></a>
## [研究人员通过电磁信号识别手机应用，准确率高达 99%](https://www.scmp.com/news/china/science/article/3359688/chinese-researchers-find-peephole-any-smartphone-its-leaked-radio-signal) ⭐️ 8.0/10

中国研究人员开发出一种非接触式技术，通过分析手机泄漏的低频电磁信号来识别正在运行的应用及部分操作，在测试设备上准确率最高达 99.07%。 这种侧信道攻击构成了重大隐私威胁，因为它无需访问设备的系统或存储数据，甚至在离线、飞行模式、加密或锁定状态下也能工作，凸显了监控和取证的新途径。 该技术在 iPhone 15 Pro、小米 15 Pro 和 OPPO Reno 13 上进行了测试，能准确识别抖音、微信视频通话、百度地图、短信、浏览器、相机和云存储等应用，最高准确率达 99.07%。

telegram · zaihuapd · 7月8日 16:05

**背景**: 智能手机在运行时会因内部电流流动而泄漏低频电磁信号。这些信号可以被远程捕获并分析，从而推断设备活动，这是一种侧信道攻击。与传统需要软件访问的方法不同，这种方法利用物理泄漏，即使设备加密或离线也能有效工作。

**标签**: `#security`, `#privacy`, `#mobile devices`, `#electromagnetic signals`, `#forensics`

---