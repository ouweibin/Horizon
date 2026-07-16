---
layout: default
title: "Horizon Summary: 2026-07-16 (ZH)"
date: 2026-07-16
lang: zh
---

> 从 33 条内容中筛选出 11 条重要资讯。

---

1. [Stripe 与 Advent 联合出价 530 亿美元收购 PayPal](#item-1) ⭐️ 9.0/10
2. [Claude web_fetch 漏洞导致记忆数据泄露](#item-2) ⭐️ 9.0/10
3. [DeepSeek 完成逾 500 亿元首轮融资，特殊架构保控制权](#item-3) ⭐️ 9.0/10
4. [xAI 起诉用户利用 Grok 制作儿童性虐待深度伪造](#item-4) ⭐️ 9.0/10
5. [Telegram 数据中心分析及 FSB 关联](#item-5) ⭐️ 8.0/10
6. [xAI 在隐私风波后开源 grok-build](#item-6) ⭐️ 8.0/10
7. [哈达玛积聚类法解开卷积神经元](#item-7) ⭐️ 8.0/10
8. [AI 伴侣应用收入超 4 亿美元，69%用户隐瞒伴侣](#item-8) ⭐️ 8.0/10
9. [美国法官质疑 Epic 与谷歌反垄断和解背后新合作](#item-9) ⭐️ 8.0/10
10. [马斯克：X 将无条件开源全部代码，接受第三方审计](#item-10) ⭐️ 8.0/10
11. [Telegram 推出机器人无服务器平台](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Stripe 与 Advent 联合出价 530 亿美元收购 PayPal](https://www.reuters.com/business/finance/stripe-advent-offer-buy-paypal-more-than-53-billion-sources-say-2026-07-15/) ⭐️ 9.0/10

据知情人士透露，Stripe 和私募股权公司 Advent International 联合出价超过 530 亿美元收购 PayPal。 此次收购将创造一个支付巨头，整合 Stripe、PayPal、Venmo、Braintree 和 Xoom，因其在在线支付领域的市场集中度而引发重大反垄断担忧。 如果交易完成，可能面临严格的反垄断审查，可能需要剥离 Venmo 或 Braintree 等资产以获得监管批准。

hackernews · rvz · 7月15日 03:32 · [社区讨论](https://news.ycombinator.com/item?id=48915953)

**背景**: 赫芬达尔-赫希曼指数（HHI）用于衡量市场集中度；Stripe 和 PayPal 合并将产生非常高的 HHI，表明反竞争风险。Stripe 是领先的在线支付处理商，而 PayPal 拥有 Venmo 和 Braintree 等流行服务。

**社区讨论**: 评论表达了对反垄断的担忧，提到高 HHI 和潜在的费用上涨。一些用户不喜欢 Stripe 的内容限制政策，担心竞争减少。其他人则认为随着卡片使用减少，整合是不可避免的。

**标签**: `#acquisition`, `#fintech`, `#Stripe`, `#PayPal`, `#antitrust`

---

<a id="item-2"></a>
## [Claude web_fetch 漏洞导致记忆数据泄露](https://simonwillison.net/2026/Jul/15/claude-web-fetch-exfiltration/#atom-everything) ⭐️ 9.0/10

研究员 Ayush Paul 发现了 Claude 的 web_fetch 工具中的一个绕过漏洞，攻击者可以通过诱使 AI 跟随来自蜜罐网站的嵌套链接，从而窃取用户的私人数据（如姓名、所在城市和雇主信息）。 该漏洞表明，即使是精心设计的数据防泄露机制也可能被绕过，对 AI 助手的用户构成严重的隐私风险。它凸显了保护处理敏感个人数据的 AI 代理所面临的持续挑战。 该攻击利用了一个漏洞：web_fetch 可以导航到先前获取页面中嵌入的 URL，从而通过一系列请求泄露数据。Anthropic 已内部识别了该问题，并通过移除 web_fetch 从其自身获取内容中跟随链接的能力进行了修复。

rss · Simon Willison · 7月15日 14:21

**背景**: “致命三重奏”指的是一种安全状况：AI 代理能够访问私有数据、遇到不可信的输入并拥有泄露渠道（如 web_fetch）。Claude 的 web_fetch 工具通常限制其只能访问用户指定或由 web_search 返回的 URL，以防止滥用。然而，允许导航到已获取内容中的链接为攻击者开辟了道路，他们可以制作蜜罐页面，诱使代理泄露数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jul/15/claude-web-fetch-exfiltration/">How I tricked Claude into leaking your deepest, darkest secrets</a></li>
<li><a href="https://www.explainx.ai/blog/claude-memory-heist-web-fetch-exfiltration-ayush-paul-july-2026">Claude Memory Heist: web_fetch PII Exfiltration - explainx.ai</a></li>
<li><a href="https://www.cyera.com/research/when-language-becomes-the-attack-vector-the-lethal-trifecta-of-ai-agents">When Language Becomes the Attack Vector: The Lethal Trifecta of AI...</a></li>

</ul>
</details>

**标签**: `#security`, `#AI`, `#data exfiltration`, `#Claude`, `#vulnerability`

---

<a id="item-3"></a>
## [DeepSeek 完成逾 500 亿元首轮融资，特殊架构保控制权](https://t.me/zaihuapd/42589) ⭐️ 9.0/10

DeepSeek 首轮融资筹得逾 500 亿元人民币（约 740 亿美元），估值超过 500 亿美元。融资采用非常规架构，投资者将资金投入 CEO 梁文锋管理的有限合伙企业，接受五年锁定期且不享有表决权。 此次巨额融资显示投资者对 DeepSeek AI 技术的极大信心。特殊架构在筹集空前资本的同时保持创始人控制权，为 AI 初创公司平衡融资与治理树立先例。 CEO 梁文锋个人投资 200 亿元。主要外部投资者包括腾讯（100 亿元）和宁德时代（50 亿元）。五年锁定期和无表决权的设计旨在最小化外部对公司决策的影响。

telegram · zaihuapd · 7月15日 12:56

**背景**: 有限合伙企业（LP）结构常用于分离控制权与经济利益。在这种安排中，普通合伙人（GP）保留全部决策权，有限合伙人（LP）出资但无表决权。这使创始人能在不稀释控制权的情况下筹集资金。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/606484520">【专业解读】有限合伙企业的架构设计要点分析 - 知乎</a></li>
<li><a href="https://www.guancha.cn/economy/2026_06_16_820663.shtml">有限合伙、五年锁定期、无投票权？传DeepSeek已完成500亿元融资</a></li>

</ul>
</details>

**标签**: `#funding`, `#AI startup`, `#DeepSeek`, `#corporate governance`, `#venture capital`

---

<a id="item-4"></a>
## [xAI 起诉用户利用 Grok 制作儿童性虐待深度伪造](https://www.reuters.com/legal/litigation/musks-xai-sues-grok-user-over-sexualized-deepfakes-2026-07-15/) ⭐️ 9.0/10

xAI 已起诉南卡罗来纳州男子 Terry Harwood，指控其利用 AI 聊天机器人 Grok 生成儿童性虐待材料和非自愿成人深度伪造，这成为首批 AI 公司因用户此类行为提起诉讼的案件之一。 此案为追究滥用 AI 工具制作违法内容的用户责任设立了潜在法律先例，可能重塑行业内的 AI 安全、监管和平台责任。 xAI 要求赔偿并申请永久禁令，禁止 Harwood 使用 Grok。该公司表示，今年已暂停 52,222 个账户，向国家失踪与受虐儿童中心举报 73,604 次，并促成至少 244 人被捕。

telegram · zaihuapd · 7月16日 01:45

**背景**: Grok 是埃隆·马斯克旗下公司 xAI 开发的 AI 聊天机器人。深度伪造技术利用生成对抗网络（GAN）通过换脸或修改内容创建逼真的假图像或视频。此案值得关注，因为它针对的是个体用户而非仅仅移除内容，可能为 AI 滥用建立新的问责标准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.pressplay.cc/project/2667A183130728C4AE30928EF3CFF4DD/articles/D2B94E6973E8BA2AF3F0B7D05D77F631">Grok 是 什 麼？ 功能特色、與ChatGPT、Gemeni... - PressPlay Academy</a></li>
<li><a href="https://www.flowhunt.io/zh/faq/what-is-grok-ai-chatbot/">什 么 是 Grok AI聊天机器人？ | FlowHunt</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#child protection`, `#legal`, `#deepfake`, `#xAI`

---

<a id="item-5"></a>
## [Telegram 数据中心分析及 FSB 关联](https://dev.moe/en/3025) ⭐️ 8.0/10

一项对 Telegram 数据中心架构的技术分析揭示了不一致性和潜在安全问题，社区讨论发现了与 FSB 基础设施的关联。 这很重要，因为它引发了对 Telegram 隐私和安全的严重担忧，尤其是对俄罗斯和乌克兰用户，并暗示可能存在政府对平台的影响。 分析指出了数据中心缺口（如 DC3），并提到 DC5 经常对中国用户不可用，而 DC2 服务俄罗斯和乌克兰用户。还提供了一种通过 Telegram API 识别用户数据中心的方法。

hackernews · theanonymousone · 7月15日 13:22 · [社区讨论](https://news.ycombinator.com/item?id=48920475)

**背景**: 根据 Telegram 的 API 文档，它使用多个数据中心（DC1-DC5）实现地理分布和可靠性。每个用户关联一个主数据中心，如果用户移动到异常位置，该数据中心可能改变。FSB（联邦安全局）是俄罗斯的主要安全机构。社区评论将 Telegram 的基础设施管理与一位也管理 FSB 基础设施的人员联系起来，Telegram 尚未公开否认这一点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Telegram_(software)">Telegram (software) - Wikipedia</a></li>
<li><a href="https://core.telegram.org/api/datacenter">Working with Different Data Centers</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了担忧：用户 vvpan 通过调查报告将 Telegram 的基础设施与 FSB 联系起来，flexagoon 指出 DC2 服务俄罗斯和乌克兰且经常宕机，glaslong 质疑缺失的 DC3 的用途，londons_explore 批评该架构为技术债务。

**标签**: `#Telegram`, `#infrastructure`, `#data centers`, `#security`, `#FSB`

---

<a id="item-6"></a>
## [xAI 在隐私风波后开源 grok-build](https://simonwillison.net/2026/Jul/15/grok-build/#atom-everything) ⭐️ 8.0/10

xAI 已将其整个 Grok Build 代码库以 Apache 2.0 许可证开源，此前其 grok CLI 工具在未经同意的情况下上传了整个用户目录，引发了严重的隐私事件。该公司还删除了所有先前保留的用户数据，并禁用了默认数据保留。 这一事件凸显了 AI 驱动开发工具中的关键隐私风险，而 xAI 迅速开源的做法是重建用户信任的罕见举措。它为 AI 编码助手领域的透明度和用户控制树立了先例。 Grok Build 代码库包含 844,530 行 Rust 代码，其中仅约 3% 为供应商代码，并包含受其他编码代理（如 Codex 和 OpenCode）启发的系统提示和工具实现。该仓库仅有一个初始提交，因此没有开发历史可供查看。

rss · Simon Willison · 7月15日 23:59

**背景**: Grok Build 是 xAI 基于终端的编码代理，由 Grok 模型驱动，专为交互式和无人值守的编码任务设计。隐私风波源于用户发现，在目录中运行 grok CLI 会将整个目录上传到 xAI 的云端，包括 SSH 密钥和密码管理器等敏感文件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://x.ai/cli">Grok Build | SpaceXAI</a></li>
<li><a href="https://docs.x.ai/build/overview">Grok Build | SpaceXAI Docs</a></li>
<li><a href="https://www.linkedin.com/pulse/grok-build-review-what-xais-new-coding-agent-actually-does-where-fojye">Grok Build Review: What xAI ’ s New Coding Agent Actually Does, and...</a></li>

</ul>
</details>

**社区讨论**: 社区反应强烈，一名用户报告称在其主目录中运行该工具会上传包括 SSH 密钥和密码在内的私人文件。埃隆·马斯克在 Twitter 上回应称，所有先前上传的用户数据将被完全删除，xAI 随后开源了代码库以恢复信任。

**标签**: `#security`, `#open source`, `#AI`, `#privacy`, `#CLI`

---

<a id="item-7"></a>
## [哈达玛积聚类法解开卷积神经元](https://www.reddit.com/r/MachineLearning/comments/1uwya70/mechanistic_interpretability_a_first_paper_on/) ⭐️ 8.0/10

一种新方法利用哈达玛积聚类法来解开 InceptionV1 中的卷积神经元，揭示了如汽车、猫和狗等单语义模式。该技术通过聚类感受野与权重的哈达玛积，暴露单个神经元检测到的多种模式。 这项工作通过提供一种细粒度分析卷积神经元的技术，推进了机械可解释性，可能有助于理解 CNN 如何表示概念。尽管作者指出语言模型更受关注，但它也可能为其他架构带来类似方法。 该方法聚类了神经元感受野与权重的哈达玛积，得到了清晰的单语义簇（如汽车）以及低激活簇（如字母），其中依赖神经元也针对同一概念激活。作者发现正负权重在依赖神经元之间均匀分布以降低整体激活，表明梯度下降有目的的行为。

reddit · r/MachineLearning · /u/narang_27 · 7月15日 06:59

**背景**: 机械可解释性旨在通过理解神经网络的内部组件来逆向工程它们。卷积神经元通常表现出多语义性，即对多个不相关的概念作出反应。哈达玛积（逐元素乘法）在此用于结合感受野和权重矩阵，从而通过聚类揭示解缠的特征。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hadamard_product_(matrices)">Hadamard product (matrices) - Wikipedia</a></li>
<li><a href="https://www.emergentmind.com/topics/monosemantic-features">Monosemantic Features in Neural Models</a></li>
<li><a href="https://www.alignmentforum.org/posts/TDqvQFks6TWutJEKu/towards-monosemanticity-decomposing-language-models-with">Towards Monosemanticity: Decomposing Language ...</a></li>

</ul>
</details>

**标签**: `#mechanistic interpretability`, `#convolutional neural networks`, `#interpretability`, `#representation learning`

---

<a id="item-8"></a>
## [AI 伴侣应用收入超 4 亿美元，69%用户隐瞒伴侣](https://decrypt.co/373395/how-much-your-boyfriend-spending-ai-girlfriends) ⭐️ 8.0/10

根据 Appfigures 数据，自 2022 年底以来，AI 伴侣应用全球累计创收 4.273 亿美元，下载量达 1.653 亿次。2026 年上半年，这些应用收入 1.628 亿美元；收入冠军 Zeta 达 3300 万美元，下载冠军 Emochi 为 790 万次。 可观的收入和用户规模凸显了 AI 伴侣技术的快速商业化，引发了关于隐私、人际关系动态和伦理设计的重要问题。69%的用户向真实伴侣隐瞒使用情况这一发现，突显了潜在的社会和情感影响。 数据由分析平台 Appfigures 提供，涵盖 214 款 AI 伴侣应用。此外，一项调查发现，15%的美国 18-30 岁有伴侣的年轻人定期使用 AI 伴侣，其中 69%的人向人类伴侣隐瞒了实际使用程度。

telegram · zaihuapd · 7月15日 10:30

**背景**: AI 伴侣应用是由大型语言模型（如 GPT-4）驱动的聊天机器人或虚拟角色，旨在提供浪漫或情感互动。它们在 2022 年底 ChatGPT 发布后获得广泛关注，引发了对生成式 AI 的更大兴趣。Appfigures 是一个追踪应用商店下载量和收入的数据平台，提供行业数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://appfigures.com/">Appfigures - ASO tools, App Intelligence, and Analytics</a></li>
<li><a href="https://zeta-ai.io/en/login">Login / Sign up - zeta</a></li>
<li><a href="https://emochi.com/topics/roleplay-app">roleplay-app | Discover AI Characters & Roleplay on Emochi</a></li>

</ul>
</details>

**标签**: `#AI`, `#companion apps`, `#social impact`, `#revenue`, `#privacy`

---

<a id="item-9"></a>
## [美国法官质疑 Epic 与谷歌反垄断和解背后新合作](https://t.me/zaihuapd/42588) ⭐️ 8.0/10

美国法官披露，Epic Games 与谷歌已达成新商业合作，涵盖联合产品开发、营销，且 Epic 将在 6 年内向谷歌支付约 8 亿美元，作为反垄断和解的一部分。 这一合作可能削弱 Epic 长期以来改革谷歌 Android 生态系统的努力，并挑战谷歌应用商店政策的主导地位，从而影响开发者和消费者。 协议涵盖 Unreal Engine、《堡垒之夜》及 Android 相关业务，由法官 James Donato 在听证会上披露，他质疑该协议是否与 Epic 的反垄断立场相冲突。

telegram · zaihuapd · 7月15日 11:15

**背景**: Epic Games 于 2020 年起诉谷歌，指控其垄断 Android 应用分发市场。该案凸显了谷歌对应用商店和支付系统的控制。Unreal Engine 是 Epic 广泛使用的游戏引擎，是许多游戏和行业的核心。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Unreal_Engine">Unreal Engine</a></li>
<li><a href="https://en.wikipedia.org/wiki/Android_(operating_system)">Android (operating system) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#antitrust`, `#Epic Games`, `#Google`, `#Android`, `#legal`

---

<a id="item-10"></a>
## [马斯克：X 将无条件开源全部代码，接受第三方审计](https://x.com/elonmusk/status/2077361679034118271) ⭐️ 8.0/10

埃隆·马斯克宣布，在完成安全漏洞审查后，X（原 Twitter）将无条件开源其全部代码库，并邀请第三方审计者验证运行中的代码与开源代码一致。 此举可能为社交媒体透明度树立新标杆，通过可验证的开放性和独立审计重建用户信任。 马斯克强调，完全透明带来的信任才是唯一值得相信的；这一承诺既包括无条件开源，也包括接受第三方审计以确认代码完整性。

telegram · zaihuapd · 7月15日 13:32

**背景**: 可重现构建是一种软件开发实践，确保相同的源代码总能产生相同的二进制文件，从而可以独立验证二进制文件是否与源代码匹配。第三方源代码审计则让外部专家审查代码中的安全漏洞、合规性和质量问题。这些实践共同构建了一条信任链，能够证明平台关于其软件的声明是真实的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Reproducible_builds">Reproducible builds</a></li>
<li><a href="https://reproducible-builds.org/">Reproducible Builds — a set of software development practices ...</a></li>

</ul>
</details>

**标签**: `#open source`, `#social media`, `#transparency`, `#Elon Musk`, `#code auditing`

---

<a id="item-11"></a>
## [Telegram 推出机器人无服务器平台](https://core.telegram.org/bots/serverless) ⭐️ 8.0/10

Telegram 正式推出无服务器服务，开发者无需管理服务器，只需一条命令即可将机器人和小程序的后端代码部署到 Telegram 的基础设施上。 这简化了机器人的开发和扩展，降低了开发者的基础设施负担，使得在 Telegram 上构建和部署机器人更加容易，可能促进第三方机器人和小程序的生态繁荣。 代码运行在紧邻 Bot API 的隔离 V8 沙箱中，自带内置 SQLite 数据库，并通过 'npx tgcloud push' 命令使用普通的 JavaScript 模块进行部署。

telegram · zaihuapd · 7月15日 16:00

**背景**: 传统上，Telegram 机器人开发者需要自行搭建和维护服务器来运行后端逻辑。这个无服务器平台消除了这一需求，利用 Telegram 现有的基础设施和 V8 JavaScript 引擎来执行代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://core.telegram.org/bots/serverless">Telegram Serverless</a></li>

</ul>
</details>

**标签**: `#Telegram`, `#Serverless`, `#Bot Development`, `#JavaScript`, `#Cloud Computing`

---