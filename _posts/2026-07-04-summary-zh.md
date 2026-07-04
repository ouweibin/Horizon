---
layout: default
title: "Horizon Summary: 2026-07-04 (ZH)"
date: 2026-07-04
lang: zh
---

> 从 47 条内容中筛选出 10 条重要资讯。

---

1. [对比解码差分从 logits 中恢复微调数据](#item-1) ⭐️ 9.0/10
2. [欧盟议会间谍软件调查员遭 Pegasus 入侵](#item-2) ⭐️ 8.0/10
3. [Wordgard：ProseMirror 创建者推出的新富文本编辑器](#item-3) ⭐️ 8.0/10
4. [Ubicloud 提倡对 PostgreSQL 使用严格内存超额提交以防止 OOM](#item-4) ⭐️ 8.0/10
5. [AI 恐惧与 LLM 导致开发者课程销售额下降超 50%](#item-5) ⭐️ 8.0/10
6. [Anthropic 指控阿里巴巴对 Claude 发动大规模蒸馏攻击](#item-6) ⭐️ 8.0/10
7. [Claude Fable 5 重新上线，安全过滤过严令开发者失望](#item-7) ⭐️ 8.0/10
8. [华为发布 Atlas 350 加速卡，搭载昇腾 950PR，性能达 H20 的 2.87 倍](#item-8) ⭐️ 8.0/10
9. [NASA 发射救援卫星提升坠落 Swift 望远镜轨道](#item-9) ⭐️ 8.0/10
10. [腾讯阿图因 AI 以不到 0.1%成本超越 Mythos](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [对比解码差分从 logits 中恢复微调数据](https://www.reddit.com/r/MachineLearning/comments/1umn2dk/contrastive_decoding_diffing_cdd_recovering/) ⭐️ 9.0/10

对比解码差分（CDD）是一种新的灰盒方法，仅通过大语言模型的 logits 恢复逐字的微调数据，无需权重访问、激活值或探测语料库。 这一突破在隐私和可解释性方面显著推进了模型差分，揭示了微调模型中的敏感训练数据，并发现了跨不相关领域反复出现的虚构角色“Elena Rodriguez 博士”等意外模式，突显了合成数据生成的风险。 CDD 使用单一默认配置，无需针对每个模型校准，在 SDF 基准测试中，跨四个模型家族（1B 到 32B 参数）的 20 个模型对中的 19 个上实现了 4+/5 的逐字恢复评分，优于需要完全权重访问且从未超过 3/5 的激活差分透镜（ADL）。

reddit · r/MachineLearning · /u/CebulkaZapiekana · 7月3日 19:01

**背景**: 模型差分是通过比较微调模型与基础模型来研究微调引入的机制变化。对比解码是一种文本生成策略，通过对比强模型和弱模型的输出来提高质量。CDD 将这一思想应用于模型差分，直接对比基础模型和微调模型的 logits，而早期方法如 ADL 需要白盒访问激活差异。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://transformer-circuits.pub/2024/model-diffing/index.html">Stage-Wise Model Diffing</a></li>
<li><a href="https://github.com/science-of-finetuning/diffing-toolkit">science-of-finetuning/diffing-toolkit - GitHub</a></li>
<li><a href="https://www.geeksforgeeks.org/nlp/contrastive-decoding-in-natural-language-processing/">Contrastive Decoding in Natural Language... - GeeksforGeeks</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#model diffing`, `#LLM`, `#interpretability`, `#privacy`

---

<a id="item-2"></a>
## [欧盟议会间谍软件调查员遭 Pegasus 入侵](https://citizenlab.ca/research/member-of-committee-investigating-spyware-hacked-with-pegasus/) ⭐️ 8.0/10

Citizen Lab 确认，一名参与调查间谍软件的欧洲议会议员的手机在 2022 年 10 月和 2023 年 3 月被 Pegasus 间谍软件感染。 这次攻击直接破坏了欧洲议会的安全，并引发了关于国家支持的监控针对调查间谍软件滥用的立法者的严重担忧。 法医分析确定了三个不同的感染日期，其中第一次感染时间与一个针对流亡欧洲的俄罗斯和白俄罗斯记者的活动重叠。

hackernews · ledoge · 7月3日 20:38 · [社区讨论](https://news.ycombinator.com/item?id=48779683)

**背景**: Pegasus 是由以色列公司 NSO Group 开发的一款强大的间谍软件，能够通过零点击漏洞远程感染移动设备。Citizen Lab 是多伦多大学著名的网络安全研究小组，广泛记录了 Pegasus 的滥用情况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Pegasus_(spyware)">Pegasus (spyware)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Citizen_Lab">Citizen Lab</a></li>

</ul>
</details>

**社区讨论**: 评论指出，希腊和其他欧盟国家曾滥用 Pegasus，暗示这次攻击可能是国内而非外部所为。一些人质疑议会为何允许在同一个设备上存储个人和工作数据。

**标签**: `#cybersecurity`, `#spyware`, `#European Parliament`, `#surveillance`, `#privacy`

---

<a id="item-3"></a>
## [Wordgard：ProseMirror 创建者推出的新富文本编辑器](https://wordgard.net/) ⭐️ 8.0/10

Wordgard 是由 ProseMirror 创建者 Marijn Haverbeke 推出的新型浏览器内富文本编辑器，提供了改进的架构和功能用于构建自定义编辑器。 这之所以重要，是因为它出自富文本编辑器生态中备受尊敬的开发者之手，可能会设定新标准或提供一种比 ProseMirror 陡峭学习曲线更易上手的替代方案。 Wordgard 与 ProseMirror 共享许多概念，但并非升级路径；切换需要大量工作。文档中包含一个与 ProseMirror 比较的页面。

hackernews · indy · 7月3日 08:50 · [社区讨论](https://news.ycombinator.com/item?id=48772573)

**背景**: ProseMirror 是一个著名的开源库，用于通过所见即所得界面创建可定制的结构化文档。它具有模块化架构，但学习曲线陡峭。Wordgard 旨在解决其中一些限制，同时保留相似的概念。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://prosemirror.net/">ProseMirror</a></li>
<li><a href="https://github.com/ProseMirror/prosemirror">ProseMirror/prosemirror: The ProseMirror WYSIWYM editor - GitHub</a></li>

</ul>
</details>

**社区讨论**: 评论显示了兴趣和实际担忧的混合。一位评论者指出从 ProseMirror 升级缺乏路径，另一位则称赞了设计。第三位讨论了在 ProseMirror 中使用静态类型时的困难，暗示 Wordgard 可能有改进。

**标签**: `#rich-text-editor`, `#prosemirror`, `#web-development`, `#editor-framework`

---

<a id="item-4"></a>
## [Ubicloud 提倡对 PostgreSQL 使用严格内存超额提交以防止 OOM](https://www.ubicloud.com/blog/postgresql-and-the-oom-killer-why-we-use-strict-memory-overcommit) ⭐️ 8.0/10

Ubicloud 发布了一篇博客文章，解释了他们为何对 PostgreSQL 使用严格内存超额提交（vm.overcommit_memory=2）以防止 OOM killer 终止数据库进程。 此事重要，因为 PostgreSQL 的内存行为使其在默认 Linux 超额提交设置下容易受到 OOM killer 的攻击，而严格超额提交可以提高生产数据库的稳定性，但需要仔细调优。 文章描述了三种超额提交模式：启发式 (0)、始终 (1) 和严格 (2)。他们建议 PostgreSQL 使用模式 2，但警告说未经测试调整超额提交比率可能会阻止 fork 并导致应用程序崩溃。

hackernews · furkansahin · 7月3日 13:00 · [社区讨论](https://news.ycombinator.com/item?id=48774509)

**背景**: Linux 内核的超额提交内存策略控制系统是否允许超出物理 RAM 的内存分配。当超额提交导致内存耗尽时，OOM killer 会终止进程以释放内存。PostgreSQL 的内存管理经常分配大量内存，使其在默认设置下成为 OOM killer 的主要目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://linuxhandbook.com/oom-killer/">What is Out of Memory Killer (OOM Killer) in Linux?</a></li>
<li><a href="https://www.baeldung.com/linux/memory-overcommitment-oom-killer">Linux Memory Overcommitment and the OOM Killer - Baeldung Understanding and Utilizing the Linux OOM Killer - linuxvox.com memory - Understanding the Linux oom-killer's logs - Stack ... How to Configure the Linux Out-of-Memory Killer - Oracle Fix: Linux OOM Killer Killing Processes (Out of Memory)</a></li>
<li><a href="https://kernel-internals.org/mm/overcommit/">Memory Overcommit - Linux Kernel Internals</a></li>

</ul>
</details>

**社区讨论**: 评论强调了不同的经验：一些人称赞严格超额提交带来的稳定性，而另一些人则警告会出现 fork 失败或系统不稳定等副作用。Ubicloud 的联合创始人承认标题过于强硬，并承认在某些场景下严格超额提交可能带来意想不到的问题。

**标签**: `#PostgreSQL`, `#OOM killer`, `#memory management`, `#Linux`, `#production databases`

---

<a id="item-5"></a>
## [AI 恐惧与 LLM 导致开发者课程销售额下降超 50%](https://simonwillison.net/2026/Jul/3/josh-w-comeau/#atom-everything) ⭐️ 8.0/10

课程创作者 Josh W. Comeau 报告称，他的新课程《Whimsical Animations》预计销量仅为正常发布的约三分之一，而他的现有课程销售也比去年大幅下降，整体降幅超过 50%。 这一第一手证据凸显了 AI 恐惧和基于 LLM 的辅导正在重塑开发者教育，可能威胁众多在线课程创作者的商业模式，并影响开发者学习新技能的方式。 Comeau 与多位课程创作者交流，他们均报告了相同的趋势：收入下降超过 50%，参与内容的人数减少，学习者转向 LLM，而 LLM 未经同意或补偿就复制了创作者的作品。

rss · Simon Willison · 7月3日 21:25

**背景**: 大型语言模型（如 GPT-4）的兴起使得 AI 工具能够回答编程问题并提供辅导，通常免费或低成本。这导致许多开发者质疑付费课程的价值，尤其是在 AI 可能取代开发者工作的担忧中。此外，这些模型在公开内容（包括在线课程）上训练，而未对原创者进行补偿。

**标签**: `#AI`, `#developer education`, `#LLMs`, `#online courses`, `#industry trends`

---

<a id="item-6"></a>
## [Anthropic 指控阿里巴巴对 Claude 发动大规模蒸馏攻击](https://t.me/zaihuapd/42327) ⭐️ 8.0/10

Anthropic 致信美国参议院银行委员会，指控阿里巴巴利用近 2.5 万个欺诈账户，在 2026 年 4 月 22 日至 6 月 5 日期间与 Claude 进行超过 2880 万次交互，发动大规模蒸馏攻击。据报道，阿里巴巴随后下令要求全体员工在 7 月 10 日前卸载所有 Claude 相关产品。 这是已知对前沿 AI 模型规模最大的蒸馏攻击，凸显了中美 AI 公司之间知识产权盗窃问题的升级。该事件暴露了公开 API 的脆弱性，可能促使全球范围内实施更严格的安全措施和监管行动。 Anthropic 通过分类器和行为指纹识别技术检测到跨大量账户的协调活动。被指控方包括阿里巴巴及其 AI 实验室 Qwen，攻击目标是窃取 Claude 的能力，可能用于复制到竞争模型中。

telegram · zaihuapd · 7月3日 06:21

**背景**: 蒸馏攻击（或称模型提取攻击）是指通过公开 API 反复查询专有 AI 模型，利用输入-输出对训练竞争模型，从而窃取其能力。此类攻击已被白宫标记为国家安全问题，尤其是在中美 AI 竞争背景下。Anthropic 等公司已建立检测系统识别这些模式，并与其他实验室共享技术指标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks">Detecting and preventing distillation attacks \ Anthropic</a></li>
<li><a href="https://www.cnbc.com/2026/06/24/anthropic-alibaba-distillation-campaign.html">Anthropic accuses Alibaba of campaign to extract AI capabilities What Are Distillation Attacks and How Can They Be Curbed AI distillation attacks in the US–China contest</a></li>
<li><a href="https://cloud.google.com/blog/topics/threat-intelligence/distillation-experimentation-integration-ai-adversarial-use">GTIG AI Threat Tracker: Distillation, Experimentation, and (Continued) Integration of AI for Adversarial Use | Google Cloud Blog</a></li>

</ul>
</details>

**标签**: `#AI安全`, `#模型蒸馏`, `#Anthropic`, `#阿里巴巴`, `#知识产权`

---

<a id="item-7"></a>
## [Claude Fable 5 重新上线，安全过滤过严令开发者失望](https://www.bleepingcomputer.com/news/artificial-intelligence/claude-fable-relaunch-disappoints-users-with-nerfed-performance/) ⭐️ 8.0/10

Anthropic 的 Claude Fable 5 在出口管制解除后重新上线，但用户报告称其安全过滤机制过于严格，错误地将合法代码归类为违规，导致模型频繁自动降级至 Opus 4.8。 这损害了开发者的信任和工作效率，因为该模型的先进能力在关键编码任务中常常无法使用，凸显了在 AI 部署中平衡安全性与可用性的挑战。 模型的核心性能并未改变，但安全防护阈值设置过高。订阅用户面临使用限制：7 月 7 日前每周仅可调用 50% 的配额，之后 Fable 5 将改为按量付费。API 和企业按量付费版仍可完整访问。

telegram · zaihuapd · 7月3日 07:20

**背景**: Claude Fable 5 是 Anthropic 的 Claude Mythos 模型的公开版本，专为高级编程任务设计。Anthropic 最初因担心该模型发现软件漏洞的能力而暂缓发布。重新上线后，公司实施了更严格的安全过滤器，导致频繁的误报，从而降低了开发者体验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI`, `#Anthropic`, `#Claude`, `#Safety`, `#Developer Experience`

---

<a id="item-8"></a>
## [华为发布 Atlas 350 加速卡，搭载昇腾 950PR，性能达 H20 的 2.87 倍](https://t.me/zaihuapd/42329) ⭐️ 8.0/10

在 2026 年华为中国合作伙伴大会上，华为正式发布并上市了搭载全新昇腾 950PR 处理器的 Atlas 350 AI 训练推理加速卡。该卡声称单卡算力达到英伟达 H20 的 2.87 倍，并且是国内唯一支持 FP4 低精度推理的加速卡。 此次发布在美制裁背景下提供了性能更优的国产替代方案，显著挑战了英伟达在 AI 硬件市场的主导地位。它使得中国企业能够在单卡上运行 70B 参数的大语言模型，从而降低推理延迟和部署成本。 Atlas 350 配备 112 GB HBM 内存，并支持 FP4 推理，从而降低内存占用并加速计算。与前代相比，其向量算力、互联带宽和自研 HBM 均有大幅提升，支持 70B 参数模型的单卡加载。

telegram · zaihuapd · 7月3日 08:35

**背景**: FP4（4 位浮点数）推理是一种低精度技术，将模型权重和激活值用 4 位格式表示，在保持精度的同时减少内存占用并提高吞吐量。华为昇腾系列是在美国出口限制下研发的 AI 芯片家族，950PR 是最新的高端推理处理器。英伟达 H20 是符合中国出口管制要求的 GPU，性能有所削减。华为 Atlas 系列加速卡面向 AI 训练和推理工作负载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tech-insider.org/huawei-ascend-950pr-ai-chip-nvidia-china-2026/">Huawei Ascend 950PR: The 1.56 PFLOP AI Chip vs Nvidia [2026]</a></li>
<li><a href="https://www.huaweicentral.com/ascend-950pr-ai-chip-everything-you-need-to-know/">Ascend 950PR AI Chip: Everything you need to know</a></li>
<li><a href="https://nerdleveltech.com/huawei-ascend-950pr-atlas-350-ai-chip-challenges-nvidia">Huawei Ascend 950PR Beats NVIDIA H20: 2.8× FP8, CUDA-Ready</a></li>

</ul>
</details>

**标签**: `#AI Hardware`, `#Huawei`, `#Ascend 950PR`, `#Accelerators`, `#FP4`

---

<a id="item-9"></a>
## [NASA 发射救援卫星提升坠落 Swift 望远镜轨道](https://apnews.com/article/swift-nasa-satellite-rescue-katalyst-a7ddd740ca099587c58865f583c7245a) ⭐️ 8.0/10

2026 年 7 月 3 日，NASA 发射了由 Katalyst Space 建造的 LINK 航天器，旨在捕获并提升老化的 Swift 伽马射线暴观测站至更高轨道，推迟其大气再入。 此次任务是私人航天器首次尝试捕获并服务美国政府卫星，可能彻底改变卫星寿命延长方式并减少太空垃圾。同时确保对伽马射线暴的科学观测持续进行。 LINK 将使用机械臂抓住 Swift，然后将其轨道提升约 240 公里。若成功，Swift 最快可在 9 月恢复观测。

telegram · zaihuapd · 7月3日 15:43

**背景**: Swift 于 2004 年发射，观测伽马射线暴，对多波段天文学至关重要。由于太阳活动导致的大气阻力，其轨道不断降低，若不干预，可能于今年 10 月坠入大气层烧毁。LINK 航天器是商业机器人服务航天器，用于卫星寿命延长。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nasa.gov/image-article/link-spacecraft-set-for-mission-to-boost-nasas-swift-observatory/">LINK Spacecraft Set for Mission to Boost NASA ’s Swift... - NASA</a></li>
<li><a href="https://www.cbsnews.com/news/nasa-mission-rescue-falling-swift-telescope/">Mission launched to save falling Swift space telescope - CBS News</a></li>
<li><a href="https://www.dw.com/en/swift-boost-mission-an-opportunity-for-science-and-defense/a-77768927">NASA 's Swift Boost mission : chance for science and defense</a></li>

</ul>
</details>

**标签**: `#space`, `#NASA`, `#satellite servicing`, `#astronomy`

---

<a id="item-10"></a>
## [腾讯阿图因 AI 以不到 0.1%成本超越 Mythos](https://mp.weixin.qq.com/s/BzU7g-2iG7d6h4ViwMhxyg) ⭐️ 8.0/10

腾讯玄武实验室基于开源模型 GLM-5.1 构建的阿图因 AI 在加州大学伯克利分校主导的 CyberGym 基准测试中获得 84%的得分，超过了 Anthropic 的 Claude Mythos Preview。它还在 curl、OpenSSL 等项目中发现了多个 Mythos 未检出的高危逻辑漏洞。 这表明开源 AI 模型能够以极低的成本在专业网络安全任务上超越闭源模型，可能使漏洞发现更加普及。同时，本地部署的模型也能发现真实世界的关键漏洞，并得到伯克利排名的验证。 阿图因 AI 消耗的预算不到 Mythos‘玻璃翼计划’的 0.1%。在伯克利 BVI 真实世界漏洞榜单中，阿图因 AI 的严重漏洞严重程度排名第 1，总数排名第 5，最高 CVSS 评分达 9.3。

telegram · zaihuapd · 7月3日 16:12

**背景**: CyberGym 是由加州大学伯克利分校创建的大规模基准测试，用于评估 AI 代理在真实世界漏洞分析任务上的能力，包含 188 个项目中的 1507 个漏洞。GLM-5.1 是智谱 AI（Z.AI）开发的开源权重大型语言模型，采用 MIT 许可证发布。Claude Mythos 是 Anthropic 为网络安全设计的专有模型，但因安全考虑尚未公开发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/sunblaze-ucb/cybergym">GitHub - sunblaze-ucb/cybergym: CyberGym is a large-scale, high-quality cybersecurity evaluation framework designed to rigorously assess the capabilities of AI agents on real-world vulnerability analysis tasks. · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/GLM-5.1">GLM-5.1</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mythos_AI">Mythos AI</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#AI`, `#Tencent`, `#open-source`, `#vulnerability discovery`

---