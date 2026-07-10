---
layout: default
title: "Horizon Summary: 2026-07-10 (ZH)"
date: 2026-07-10
lang: zh
---

> 从 38 条内容中筛选出 11 条重要资讯。

---

1. [OpenAI 发布 GPT-5.6，在 ARC-AGI-3 上达到 SOTA](#item-1) ⭐️ 9.0/10
2. [TypeScript 7.0 正式发布，Go 重写带来最高 12 倍速度提升](#item-2) ⭐️ 9.0/10
3. [Colibrì 在 32GB 内存的笔记本上运行 GLM 5.2](#item-3) ⭐️ 8.0/10
4. [欧盟议会批准聊天控制 1.0](#item-4) ⭐️ 8.0/10
5. [用 Rust 重写的 PostgreSQL 通过所有回归测试](#item-5) ⭐️ 8.0/10
6. [Meta 发布 Muse Spark 1.1，包含定价和评估](#item-6) ⭐️ 8.0/10
7. [Meta 超级智能一年进展：前所未有的算力扩展和 2000 公里互连](#item-7) ⭐️ 8.0/10
8. [蚂蚁开源灵波 LingBot-Video：全球首个 MoE 具身视频基模](#item-8) ⭐️ 8.0/10
9. [大疆 EV50 飞越珠峰创 8861 米高度纪录](#item-9) ⭐️ 8.0/10
10. [国家超算互联网核心节点在郑州上线](#item-10) ⭐️ 8.0/10
11. [OpenAI 与美国战争部同意禁止 AI 用于国内监控](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-5.6，在 ARC-AGI-3 上达到 SOTA](https://openai.com/index/gpt-5-6/) ⭐️ 9.0/10

OpenAI 发布了其最新旗舰模型 GPT-5.6，提供三种规模（Luna、Terra、Sol），在交互式推理基准 ARC-AGI-3 上取得了 7.8% 的新最高分，并引入了改进的意图理解和原始图像保留功能。 GPT-5.6 在旨在衡量类人交互推理能力的基准上超越了以往模型，为 AI 推理和主体智能树立了新标杆。此次发布可能影响 AI 行业向更自主、更理解用户目标的系统方向发展。 GPT-5.6 按每百万 token 定价：Luna 输入 $1/输出 $6，Terra $2.50/$15，Sol $5/$30。该模型还提供了使用意图理解的语义提示——开发者应明确指定约束条件，而模型会推断目标；同时图像输入会保留原始尺寸。

hackernews · logickkk1 · 7月9日 17:04 · [社区讨论](https://news.ycombinator.com/item?id=48849066)

**背景**: ARC-AGI-3 是一个交互式推理基准，挑战 AI 智能体探索新环境、推断目标并规划行动——通过回合制抽象任务来衡量类人智能。意图理解指的是 AI 能够超越字面措辞推断用户的深层目标，从而改善对话式 AI 的上下文响应。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://businesslibrary.uflib.ufl.edu/thinking-like-an-ai-intent">AI Intent - Thinking Like an AI: Understanding "Intent" - UF Business Library at University of Florida</a></li>

</ul>
</details>

**社区讨论**: 社区评论强调了开发者指南中关于意图理解和图像保留的提示，注意到了 BenchCAD 上的高分，并确认了 GPT-5.6 Sol 在 ARC-AGI-3 上的 SOTA 成绩。一些用户指出 Fable 5 因拒绝回答高级生物学问题而被排除在比较之外，而另一些用户则讨论是否应从 Claude Code 转向 Codex 用于编码任务。

**标签**: `#AI`, `#GPT-5.6`, `#OpenAI`, `#large language models`, `#benchmarking`

---

<a id="item-2"></a>
## [TypeScript 7.0 正式发布，Go 重写带来最高 12 倍速度提升](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 9.0/10

微软正式发布 TypeScript 7.0，这是用 Go 语言重写的原生版本，完整构建速度比旧版快 8 到 12 倍，并支持共享内存多线程。用户可通过 npm 安装，主流编辑器通过 LSP 支持新语言服务器。 该版本大幅缩短构建时间，显著提升开发者效率，对大型代码库尤为重要。Go 重写标志着编译器实现策略的重大转变，可能影响未来语言工具链的发展方向。 新引入 --checkers 和 --builders 参数以自定义类型检查和项目引用构建的并行度。提供兼容包实现与 TypeScript 6 并存，但 Vue、Svelte 等嵌入式语言工具链因 API 尚未就绪，仍需使用旧版本。

telegram · zaihuapd · 7月9日 04:01

**背景**: TypeScript 是微软开发的 JavaScript 静态类型超集。之前的编译器由 TypeScript 本身编写，大型项目下可能变慢。语言服务器协议（LSP）标准化了编辑器与语言服务器之间的通信，从而支持代码智能功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/">Announcing TypeScript 7.0 - TypeScript</a></li>
<li><a href="https://en.wikipedia.org/wiki/Language_Server_Protocol">Language Server Protocol - Wikipedia</a></li>
<li><a href="https://devblogs.microsoft.com/typescript/announcing-typescript-7-0-rc/">Announcing TypeScript 7.0 RC - TypeScript</a></li>

</ul>
</details>

**标签**: `#TypeScript`, `#Go`, `#performance`, `#compiler`, `#Microsoft`

---

<a id="item-3"></a>
## [Colibrì 在 32GB 内存的笔记本上运行 GLM 5.2](https://github.com/JustVugg/colibri) ⭐️ 8.0/10

开发者 JustVugg 发布了 Colibrì，这是一个轻量级 C 引擎，通过 int4 量化以及按需从磁盘流式传输 MoE 专家权重，在 32GB 内存的笔记本上运行 744B 参数的 GLM 5.2 模型，冷启动速度达到 0.1 token/秒。 这证明了即使是非常大的 MoE 模型也可以在无 GPU 的消费级硬件上运行，扩展了本地 AI 推理的可行性，并激发了社区对进一步优化的兴趣。 密集部分（约 17B 参数）以 int4 精度常驻内存（约 9.9 GB），而 21,504 个路由专家（每个约 19 MB）存储在磁盘上（总计约 370 GB），按需流式传输，并带有每层 LRU 缓存。引擎是一个单独的 C 文件，无运行时依赖。

hackernews · vforno · 7月9日 08:05 · [社区讨论](https://news.ycombinator.com/item?id=48842459)

**背景**: GLM 5.2 是一个混合专家（MoE）大语言模型，总参数量 744B，但每个 token 仅激活约 40B 参数。Int4 量化可将模型大小减少约 4 倍，使更大模型适合内存。开发者的方法利用基于磁盘的专家流式传输和缓存，克服低端硬件的 RAM 限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/zai-org/GLM-5.2">zai-org/GLM-5.2 · Hugging Face</a></li>
<li><a href="https://docs.z.ai/guides/llm/glm-5.2">GLM-5.2 - Overview - Z.AI DEVELOPER DOCUMENT</a></li>
<li><a href="https://huggingface.co/docs/transformers/quantization/concept_guide">Quantization concepts · Hugging Face</a></li>

</ul>
</details>

**社区讨论**: 社区评论总体积极，称赞工程努力。一些人对 0.1 token/秒的实际可用性提出疑问，而其他人分享了类似项目（例如 Apple Silicon 上的 Unsloth、用于图像/视频生成的 thinfer）。总体情绪是好奇且印象深刻。

**标签**: `#LLM`, `#GLM`, `#local inference`, `#optimization`, `#AI`

---

<a id="item-4"></a>
## [欧盟议会批准聊天控制 1.0](https://www.patrick-breyer.de/en/eu-parliament-greenlights-chat-control-1-0-breyer-our-children-lose-out/) ⭐️ 8.0/10

欧洲议会批准了聊天控制 1.0，该措施允许美国科技公司在 2028 年前无需授权即可扫描私人消息，尽管该措施在 3 月份已被两次否决。 这为大规模监控树立了危险先例，削弱了数亿欧盟公民的隐私和数字权利，并引发了对民主合法性和程序操纵的严重担忧。 投票在夏季休会前的最后一天以紧急程序进行，需要 361 票的绝对多数才能否决；仅有 314 票反对，因此该措施默认通过。目前仅影响未加密消息，但批评者警告范围可能扩大。

hackernews · rapnie · 7月9日 11:03 · [社区讨论](https://news.ycombinator.com/item?id=48843923)

**背景**: “聊天控制”指欧盟通过扫描私人通信来打击儿童性虐待材料的提案。聊天控制 1.0 是对《电子隐私指令》的临时豁免，允许平台自愿扫描消息；聊天控制 2.0 是一项仍在谈判中的更长期法规。欧盟在 3 月份曾否决类似的强制扫描要求，但程序性策略使 1.0 得以复活。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fightchatcontrol.eu/chat-control-overview">Chat Control 1 . 0 vs 2.0 - Fight Chat Control</a></li>
<li><a href="https://overcentral.com/en/eu-parliament-chat-control-revival/">EU Parliament Revives Private Message Scanning Law</a></li>

</ul>
</details>

**社区讨论**: 评论者对议会策略表示愤怒，指出投票时间被安排以减少反对，且多数投票的欧洲议会议员反对该措施。他们批评民主规范受到侵蚀，并警告欧盟正走向极权主义。

**标签**: `#EU policy`, `#privacy`, `#surveillance`, `#chat control`

---

<a id="item-5"></a>
## [用 Rust 重写的 PostgreSQL 通过所有回归测试](https://github.com/malisper/pgrust) ⭐️ 8.0/10

pgrust 项目使用 LLM 辅助将 PostgreSQL 用 Rust 重写，现已通过所有 Postgres 回归测试。作者一直在尝试使用 LLM 构建更好版本的 Postgres，并正在开发一个包含更多技术的新未发布版本。 这一成就展示了使用 LLM 进行大规模系统重写的潜力，可能带来更内存安全和高效的 PostgreSQL。它也引发了关于数据库开发未来以及 AI 在系统编程中作用的讨论。 该项目在不到一个月内生成了 7101 次提交，全部由 LLM 生成。作者正在开发一个纳入所学技术的新版本，且项目的许可证可能与 PostgreSQL 不同。

hackernews · SweetSoftPillow · 7月9日 06:18 · [社区讨论](https://news.ycombinator.com/item?id=48841676)

**背景**: PostgreSQL 是一个有 30 年历史的开源关系数据库管理系统。用以内存安全和并发著称的 Rust 语言重写，有望提升安全性和性能。LLM（大语言模型）被用于辅助生成 Rust 代码，从而实现了快速开发。

**社区讨论**: 评论中既有赞赏也有质疑。一些人赞扬 LLM 的使用和技术成就，而另一些人则质疑项目的长期可持续性、代码可审查性和许可证问题。作者澄清了项目的实验性质及未来计划。

**标签**: `#database`, `#rust`, `#postgresql`, `#llm`, `#software-engineering`

---

<a id="item-6"></a>
## [Meta 发布 Muse Spark 1.1，包含定价和评估](https://ai.meta.com/blog/introducing-muse-spark-meta-model-api/) ⭐️ 8.0/10

Meta 宣布了 Muse Spark 1.1，这是一个代理式 AI 模型，新定价为每百万 token 1.25/4.5 美元，并附带详细的评估报告。 此次发布标志着 Meta 开始对代理式 AI 进行商业化，可能降低开发者成本，并加剧与 OpenAI 和 Anthropic 等闭源领先者的竞争。 模型输入每百万 token 收费 1.25 美元，输出每百万 token 收费 4.5 美元，缓存输入为 0.15 美元；评估使用自定工具，配备 6 核 CPU 和 8GB 内存，有评论指出这违反了 Terminal-Bench 2.1 的官方任务限制。

hackernews · ot · 7月9日 14:10 · [社区讨论](https://news.ycombinator.com/item?id=48846184)

**背景**: 代理式 AI 模型超越了简单的内容生成，能够使用工具、多智能体编排和推理来执行任务。Muse Spark 是 Meta 首个原生多模态代理模型，支持文本、图像和语音输入，上下文窗口为 26.2 万 token。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai.meta.com/blog/introducing-muse-spark-msl/">Introducing Muse Spark: Scaling Towards Personal Superintelligence</a></li>
<li><a href="https://grokipedia.com/page/Muse_Spark_AI_model">Muse Spark (AI model)</a></li>
<li><a href="https://artificialanalysis.ai/models/muse-spark">Muse Spark - Intelligence, Performance & Price Analysis</a></li>

</ul>
</details>

**社区讨论**: 社区反应包括实际应用（例如 simonw 创建了 LLM 插件）、对评估的批评（GodelNumbering 指出测试工具绕过了任务限制）以及策略讨论（jacobgold 建议 Meta 通过开源来削弱竞争对手；alightsoul 认为闭源模型无关紧要）。

**标签**: `#Meta`, `#Muse Spark`, `#agentic AI`, `#AI model release`, `#large language models`

---

<a id="item-7"></a>
## [Meta 超级智能一年进展：前所未有的算力扩展和 2000 公里互连](https://newsletter.semianalysis.com/p/the-future-of-meta-superintelligence) ⭐️ 8.0/10

Meta 超级智能实验室发布了一年进展更新，描述了前所未有的大规模算力扩展，涉及 2000 公里以上的互连以实现跨区域超级计算，以及一家顶级强化学习环境初创公司的出现。 这一更新表明 Meta 正大力推动超级智能发展，可能超越 Google 和 OpenAI 等竞争对手。基础设施的规模和新型互连技术可能定义下一代 AI 训练能力。 算力扩展被描述为有史以来最激进的，互连距离超过 2000 公里。文章还向 Google DeepMind 提供了战略建议，显示了竞争定位。

rss · Semianalysis · 7月9日 19:16

**背景**: Meta 超级智能实验室成立于 2025 年中，专注于实现通用人工智能和超级智能。‘跨区域扩展’方法指将相距数百公里的多个数据中心连接成一个超级计算机，这需要超长距离互连。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/the-future-of-meta-superintelligence">The Future of Meta Superintelligence: A 1 Year Progress Update</a></li>
<li><a href="https://en.wikipedia.org/wiki/Meta_Superintelligence_Labs">Meta Superintelligence Labs - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2509.17158v1">ARE: scaling up agent environments and evaluations</a></li>

</ul>
</details>

**标签**: `#Meta`, `#AI infrastructure`, `#superintelligence`, `#reinforcement learning`, `#compute scaling`

---

<a id="item-8"></a>
## [蚂蚁开源灵波 LingBot-Video：全球首个 MoE 具身视频基模](https://www.qbitai.com/2026/07/446458.html) ⭐️ 8.0/10

蚂蚁灵波开源了 LingBot-Video，这是全球首个基于 MoE 架构的具身视频基础模型，总参数 30B，推理时仅激活 3B，在 RBench 上以 0.620 总分取得最优。 该模型大幅提升推理效率，约为同等规模稠密模型的 3 倍，同时保持高性能，使具身视频生成对机器人研究和应用更加可及。 LingBot-Video 采用 DiT+MoE 架构，使用包含 7 万小时具身数据的数据集，以及关注物理合理性和任务完成度的多维强化学习奖励系统，以 Apache 2.0 许可证在 GitHub 上开源。

telegram · zaihuapd · 7月9日 04:30

**背景**: 混合专家模型（MoE）是一种机器学习技术，通过门控网络为每个输入激活多个专门子网络（专家），从而实现更大的模型容量和更低的计算成本。扩散 Transformer（DiT）将扩散模型与 Transformer 架构相结合，用于高质量视频生成。具身智能专注于能够感知并在物理环境中行动的模型，如机器人。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://lilianweng.github.io/posts/2024-04-12-diffusion-video/">Diffusion Models for Video Generation | Lil'Log</a></li>

</ul>
</details>

**标签**: `#MoE`, `#embodied AI`, `#video generation`, `#robotics`, `#open-source`

---

<a id="item-9"></a>
## [大疆 EV50 飞越珠峰创 8861 米高度纪录](https://www.163.com/dy/article/L1CUCV940514R9OJ.html) ⭐️ 8.0/10

大疆尚未发布的 EV50 垂直起降运载无人机在“巅峰使命”珠峰科考任务中，飞越珠峰北坡海拔 8861 米，创下同类无人机公开测试的最高飞行升限，并获取了 8000 米以上的大气剖面数据。 这一成就展示了大疆在极端环境下的先进无人机能力，为高空科学研究和百公里级货运等商业低空物流场景铺平了道路。 EV50 是一款复合翼垂直起降无人机，可原地垂直起降，起飞后切换固定翼巡航。在为期 12 天的任务中，它累计完成 32 架次起降，连续爬升 3730 米，返程时仍剩余 30% 电量。

telegram · zaihuapd · 7月9日 06:00

**背景**: 垂直起降（VTOL）无人机结合了垂直起降的灵活性和固定翼飞行的效率，非常适合长距离货运。EV50 空载最大航程 150 公里，最大载重 50 千克。在珠峰附近创下高度纪录，验证了其在稀薄空气和极寒环境下的性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.dji.com/cn/ev50">DJI EV 50 - 大疆首款垂直起降运载 无 人 机 - DJI 大疆创新</a></li>

</ul>
</details>

**标签**: `#drone`, `#DJI`, `#aviation`, `#technology`, `#record`

---

<a id="item-10"></a>
## [国家超算互联网核心节点在郑州上线](https://36kr.com/newsflashes/3887797387344387) ⭐️ 8.0/10

2026 年 7 月 9 日，在河南省人工智能大会上，国家超算互联网核心节点在郑州正式上线运行，可提供超过 10 万张国产人工智能算力卡。 该节点是国家超算互联网平台上线以来接入的最大规模单体国产 AI 算力资源池，极大增强了中国在 AI 发展中聚合和调度计算资源的能力。 该项目以构建覆盖全国的计算资源统筹调度体系为目标，承担运营管理、资源调度等核心功能，同时整合供需对接、产业孵化等综合服务。

telegram · zaihuapd · 7月9日 07:00

**背景**: 国家超算互联网是一个国家级项目，旨在连接全国各地的超算中心，实现计算资源的统一调度和共享。其目标是为科研、人工智能开发等领域提供高性能计算能力。

**标签**: `#supercomputing`, `#AI infrastructure`, `#China`, `#computing power`, `#national supercomputer`

---

<a id="item-11"></a>
## [OpenAI 与美国战争部同意禁止 AI 用于国内监控](https://t.me/zaihuapd/42459) ⭐️ 8.0/10

OpenAI 与美国战争部（原国防部）已原则上同意修订双方的 AI 合作协议，明确禁止将 AI 用于对美国公民进行国内监控。该修订条款由 OpenAI 首席执行官 Sam Altman 主动提出，禁止利用商业获取的个人身份信息进行蓄意监控或追踪。 这一政策发展为政府合同中的 AI 伦理使用树立了先例，回应了公民自由方面的担忧，并可能影响未来 AI 公司与国家行为者之间的协议。它表明企业在防止大规模监控技术被用于针对公民方面正承担起越来越多的责任。 修订后的条款明确禁止对美国公民进行蓄意监控，并禁止利用商业获取的个人身份信息进行追踪。该协议条款尚未正式签署，此前 Anthropic 与战争部的类似合作协议曾因类似争议而中止。

telegram · zaihuapd · 7月9日 13:22

**背景**: 美国战争部是 1789 年至 1947 年间负责美国陆军的内阁部门，1947 年根据《国家安全法案》拆分为陆军部和空军部，后由国防部接替。新闻中提及的“战争部”实为现代五角大楼的历史称呼。随着 OpenAI 和 Anthropic 等公司与军事机构合作，AI 伦理争议加剧，引发了关于监控和人权问题的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/US_Department_of_War">US Department of War</a></li>

</ul>
</details>

**标签**: `#AI ethics`, `#OpenAI`, `#US government`, `#surveillance`, `#policy`

---