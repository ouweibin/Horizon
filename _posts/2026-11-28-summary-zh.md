---
layout: default
title: "Horizon Summary: 2026-11-28 (ZH)"
date: 2026-11-28
lang: zh
---

> 从 28 条内容中筛选出 7 条重要资讯。

---

1. [OpenSec 披露 Linux 内核 NFS 服务器 CVSS 9.8 预认证 root 漏洞](#item-1) ⭐️ 9.0/10
2. [谷歌提出深度交叉注意力 DCA，改造 Transformer 残差连接，实现最高 3 倍加速](#item-2) ⭐️ 8.0/10
3. [热门购物网站发现利用 WebRTC 的信用卡盗刷脚本](#item-3) ⭐️ 8.0/10
4. [Convex 编程技能被指未经告知上传用户的应用创意](#item-4) ⭐️ 8.0/10
5. [多州总检察长起诉 SpaceX，指控 Grok 生成儿童性虐待与报复性色情图像](#item-5) ⭐️ 8.0/10
6. [SemiAnalysis：Trainium3 推理性能 TCO 优于 GB300](#item-6) ⭐️ 8.0/10
7. [Minecraft Java 版曝 Minecraft2Shell 远程代码执行漏洞，恶意资源包字体可入侵客户端](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenSec 披露 Linux 内核 NFS 服务器 CVSS 9.8 预认证 root 漏洞](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 9.0/10

OpenSec 公开了 CVE-2026-99362 的细节：这是 Linux 内核 NFS 服务器守护进程 nfsd 中的一个 CVSS 9.8 评分的预认证堆溢出漏洞，攻击者无需登录，只需一条发往 tcp/2049 的连接即可越过内核堆对象边界写入 61 字节，并可通过链式利用最终获得 root shell。该漏洞自 2014 年的 Linux 3.16 起就已存在，影响所有启用 NFSv4.1 或 4.2 的主机，修复已在内核 6.12.117、6.18.61、7.3.2 和 7.4-rc1 中发布。 NFS 是企业与家庭环境中部署最广泛的网络文件系统之一，因此该漏洞可能使文件服务器、NAS 设备以及集群存储节点面临无需登录、无需用户交互即可被远程完全接管的危险。由于缺陷代码位于内核之中且可追溯到 2014 年之前，大量长期支持版发行版和嵌入式存储设备都需要升级内核并重启，因此这是急需处理的修补优先级。 利用该漏洞的前提是主机在可访问的 tcp/2049 上提供 NFSv4.1 或 4.2 服务，且溢出本身仅在内核堆对象之后越界写入 61 字节，因此要形成可用的 root 利用需要堆布局塑造与链式组合，而非一次写入即可完成。公告指出，无法立即重启升级的管理员应通过防火墙限制对 tcp/2049 的访问作为缓解措施；该 CVE 于 2026 年 11 月 20 日公开。

telegram · zaihuapd · 11月27日 12:57

**背景**: NFS（网络文件系统）是一种允许一台机器通过网络挂载并使用另一台机器上目录的协议，在 Linux 中其服务端逻辑主要由内核里的 nfsd 组件实现，而非纯粹的用户态守护进程。NFSv4.1 与 4.2 是该协议的现代版本，新增了会话中继、服务端复制等特性，并监听 TCP 的 2049 端口。堆溢出是一种内存安全缺陷：写入的数据超过堆上缓冲区所能容纳的大小，从而破坏相邻的内核数据结构；而“预认证”意味着这种破坏发生在连接或协议处理阶段、在任何凭据校验之前，因此攻击者无需任何账号或密码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opensec.in/blog/nfs2root-cve-2026-99362">NFS2ROOT (CVE-2026-99362): pre - auth root in Linux nfsd | OpenSec</a></li>
<li><a href="https://wiki.archlinux.org/title/NFS">NFS - ArchWiki</a></li>

</ul>
</details>

**标签**: `#Linux kernel`, `#NFS`, `#security vulnerability`, `#CVE`, `#remote privilege escalation`

---

<a id="item-2"></a>
## [谷歌提出深度交叉注意力 DCA，改造 Transformer 残差连接，实现最高 3 倍加速](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 8.0/10

谷歌研究院发布博客，提出“深度交叉注意力”（Depth-wise Cross-Attention，DCA），重新设计 Transformer 的残差连接：每个 token 不再只是把上一层输出相加，而是对所有先前层的嵌入做注意力加权聚合。据其报告，DCA 在模型质量相当的情况下，训练和推理速度最高可提升 3 倍，也就是单位 FLOP 所换来的质量更高。 自 2017 年原始 Transformer 以来，残差（跳跃）连接几乎从未变过，因此一种更省算力的加深网络层数的方法，会影响所有训练或部署大语言模型的人。如果这种“每 FLOP 质量”提升在更大规模上依然成立，它将直接降低训练算力成本与推理延迟，也可能让 Gemini 这类模型运行得更便宜、更快。 DCA 对 Q/K/V 做了拆分，使注意力作用在“深度”（层）方向而不只是 token 序列方向：每个 token 都会对所有先前层嵌入做动态加权的混合查询，从而避免在更长 token 序列上扩展注意力所带来的二次方开销。这些结论来自谷歌自己在语言建模任务上的基准测试，因此独立复现以及在前沿规模下的表现仍有待验证。

hackernews · ComputedCamp995 · 11月27日 23:06 · [社区讨论](https://news.ycombinator.com/item?id=50672565)

**背景**: Transformer 由一叠相同的模块堆叠而成，每个模块包含一个在序列内不同 token 之间混合信息的注意力子层，以及一个逐 token 处理的前馈子层。残差连接最早随 2015 年的 ResNet 出现，它把模块的输入加回输出，使梯度能穿过几十甚至上百层而不消失；在标准 Transformer 中，每个模块只能看到紧邻上一层的输出。FLOPs（浮点运算次数）是研究者衡量计算成本的硬件无关指标，因此“每 FLOP 质量”比较的是不同架构在固定算力下能换来多少模型质量。DCA 把原本简单的加法式跳跃连接，改成了对所有历史层嵌入的学习式注意力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections</a></li>
<li><a href="https://poloclub.github.io/transformer-explainer/">Transformer Explainer: LLM Transformer Model Visually Explained</a></li>
<li><a href="https://blog.authon.dev/standard-transformer-attention-vs-attention-residuals-a-practical-comparison">Standard Transformer Attention vs. Attention- Residuals ... | Authon Blog</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论整体偏正面：有用户称 Gemini“Neon”相对 Claude Opus 便宜、快速得惊人，并猜测这是否与 DCA 有关；还有人认为对所有先前层做注意力，或许终于能解决著名的“strawberry”计数/推理失败问题。也有人把它与 DenseNet 的密集连接相类比，并顺带吐槽结果图表应该用柱状图而不是折线图。

**标签**: `#transformers`, `#llm-architecture`, `#google-research`, `#attention-mechanisms`, `#training-efficiency`

---

<a id="item-3"></a>
## [热门购物网站发现利用 WebRTC 的信用卡盗刷脚本](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 8.0/10

研究人员在热门购物网站上发现了滥用 WebRTC 的信用卡盗刷脚本，该活动据称选在黑色星期五前后发动；这些脚本主要针对移动端用户，并利用 WebRTC 规避检测。 这一发现凸显了电商网站上的第三方脚本仍是重大的供应链风险，也表明攻击者可以在购物旺季利用较少被审查的浏览器 API 绕过常规监控。 WebRTC 本身是合法的实时通信 API，因此问题不在于 WebRTC 存在漏洞，而在于其数据通道很少被审查；评论者指出，同样的数据外传也可以用普通 HTTP 请求完成，而针对移动端则让检测更加困难。提供的摘要没有点名受影响的零售商，也没有给出受感染网站的数量。

hackernews · scanr · 11月27日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50668145)

**背景**: WebRTC（Web 实时通信）是一个开源的浏览器 API，用于点对点的音频、视频和数据通信，由 W3C 和 IETF 制定标准，并得到 Apple、Google、Microsoft、Mozilla 和 Opera 的支持。信用卡盗刷脚本通常被称为 Magecart 脚本，是注入在线商店的 JavaScript，用于在顾客输入时窃取支付卡数据。许多电商网站会加载数十个用于分析、广告和聊天组件的第三方脚本，这大大扩大了攻击面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebRTC">WebRTC</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-abuse-google-apps-script-to-steal-credit-cards-bypass-csp/">Hackers abuse Google Apps Script to steal credit cards , bypass CSP</a></li>
<li><a href="https://www.zdnet.com/article/inter-a-low-bar-kit-for-magecart-website-credit-card-skimmer-attacks/">Inter: a ‘low bar’ kit for Magecart credit card skimmer attacks... - ZDNET</a></li>

</ul>
</details>

**社区讨论**: 评论者认为这一事件证明了拦截广告和脚本的合理性，同时有几个人指出 WebRTC 在技术上并不特殊——只是其通道较少被监控，而普通 HTTP 也能实现同样的窃取。还有人批评 Web 在浏览器中运行第三方代码的模式，并质疑广告网络和浏览器为何不对广告进行沙箱隔离或禁止其执行 JavaScript。

**标签**: `#security`, `#web-security`, `#e-commerce`, `#skimming`, `#WebRTC`

---

<a id="item-4"></a>
## [Convex 编程技能被指未经告知上传用户的应用创意](https://github.com/convex/convex-backend-skill/issues/64) ⭐️ 8.0/10

一份 GitHub issue（convex/convex-backend-skill#64）指控 Convex 的 AI 编程技能会在用户不知情的情况下，把用户的应用创意和提示词静默上传到远程服务器。该问题登上 Hacker News 首页，获得约 269 分和 87 条评论，Convex 首席执行官 Jamie 也在讨论串中作出回应，说明这次上传的用途。 AI 编程“技能”是纯指令包，会被 Claude Code、Cursor、Codex 等智能体自动加载并执行，因此其中隐藏的网络请求同时触及用户隐私和整个技能分发生态的信任基础。又因为 Convex 本身还托管客户的数据与代码并运营 AI 网关，这场争议进一步引出一个更宏观的问题：对于处在 AI 工具链中的厂商，默认应当给予多少信任。 首席执行官 Jamie 在讨论中解释，这次提示词上传是为 Convex 的“quickstart”（快速上手）功能服务，他称该功能是 Convex 近期关停的端到端“vibe-coding”产品 Convex Chef 的精神继任者。评论者指出，这场争议混淆了两种不同的风险：一种是厂商有意的数据收集，另一种是提示词注入（prompt injection）；不少人认为后者远比模型自行发起恶意工具调用更为常见。

hackernews · MickyTheMouse · 11月27日 18:02 · [社区讨论](https://news.ycombinator.com/item?id=50669765)

**背景**: Convex 是一个后端即服务（BaaS）平台，提供响应式数据库、无服务器函数、文件存储、搜索以及 AI 网关，让开发者无需自行管理服务器就能构建并托管应用。AI“编程技能”则是一套打包好的指令，开发者把它装进 AI 编程智能体中，让智能体知道如何正确使用某个产品；这类技能通过技能中心和市场分发，并以智能体本身已有的权限运行。提示词注入（prompt injection）是一种攻击方式：来自用户或模型所读取外部数据中的精心构造文本被误当成可信指令，导致模型偏离原本的行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.convex.dev/">Convex | All gas, no breakages</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection - Wikipedia</a></li>
<li><a href="https://terminalskills.io/skills/convex">Convex — AI Agent Skill | Terminal Skills</a></li>

</ul>
</details>

**社区讨论**: 讨论整体持怀疑态度但并非敌意：有人认为从长远看，自托管的开放权重模型才是解决这类信任问题的出路，也有人指出提示词注入远比模型自行发起恶意工具调用更常见。另一些人则从声誉角度解读此事，评论称“信任才是新的注意力”，还有人对自己在 issue 评论区看到某位 YouTube 作者推广其个人媒体网站感到困惑。首席执行官直接而坦率的回应总体上被视为积极信号，而非敷衍了事。

**标签**: `#privacy`, `#AI-tooling`, `#security`, `#prompt-injection`, `#developer-tools`

---

<a id="item-5"></a>
## [多州总检察长起诉 SpaceX，指控 Grok 生成儿童性虐待与报复性色情图像](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 8.0/10

由弗吉尼亚州总检察长 Jay Jones 和俄勒冈州总检察长 Rayfield 牵头的多州总检察长联盟，对 SpaceX（诉状中称其为 X、xAI 和 Grok 的母公司）提起诉讼，指控该聊天机器人生成并助长儿童性虐待材料（CSAM）以及未经同意的私密图像。诉讼针对的是平台的内容审核失职，而非某一个用户的具体提示词。 这是首批针对 AI 图像生成模型输出内容的多州执法行动之一，将检验当模型可被诱导生成违法内容时，平台与母公司的责任边界能延伸到何处。其判决结果可能为所有面向消费者的图像生成功能设定内容审核要求与默认安全措施，同时也正好落在 AI 安全监管与第一修正案保护之间尚未有定论的法律地带。 诉状同时聚焦于 CSAM 和未经同意的私密图像的生成，以及该公司涉嫌对这些能力的推广；xAI 的 Grok 自带图像生成功能，此前已多次因防护措施薄弱而受到审视。一个关键的法律难点在于：未经同意的私密图像在定义上必然描绘或指向真实人物，因此不受最高法院对纯合成图像所做豁免的保护。

hackernews · DeepLogin · 11月27日 19:42 · [社区讨论](https://news.ycombinator.com/item?id=50670855)

**背景**: Grok 是埃隆·马斯克旗下 xAI 开发的大语言模型，该公司还提供图像生成功能，并与 X 社交平台深度集成。美国法律把 CSAM 视为基本不受保护的言论，但在 2002 年的 Ashcroft 诉 Free Speech Coalition 案中，最高法院推翻了禁止未使用、未描绘真实儿童的“虚拟儿童色情”的联邦条款——这一判例如今正被拿来围绕 AI 生成内容展开争论。另一方面，多数州都制定了禁止未经同意的私密图像（“报复性色情”）的法律，平台通常依赖自动分类器和内容审核 API 在内容发布前进行检测与拦截。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sightengine.com/detect-ai-generated-images">AI Image Detector. Detect AI - Generated Images</a></li>
<li><a href="https://beatapi.io/content-moderation-api">AI Content Moderation API for Text and Images | BeatAPI</a></li>

</ul>
</details>

**社区讨论**: 评论者在成因与责任归属上意见分歧：有人困惑于 Grok 究竟是默认就很宽松，还是必须被刻意“越狱”才能生成此类内容；也有人认为应当被追责的是实际生成这些材料的人。最有实质内容的一条讨论援引了 Ashcroft 诉 Free Speech Coalition 案，认为不描绘真实儿童的、自行生成的合成 CSAM 属于受保护的言论，但同时承认未经同意的私密图像性质不同，因为它必然涉及真实人物。

**标签**: `#AI safety`, `#AI regulation`, `#xAI/Grok`, `#content moderation`, `#free speech law`

---

<a id="item-6"></a>
## [SemiAnalysis：Trainium3 推理性能 TCO 优于 GB300](https://newsletter.semianalysis.com/p/trainium3-inferencex) ⭐️ 8.0/10

SemiAnalysis 发布了对 AWS Trainium3 推理性能与微架构的深度分析，称其在 UBenchX 基准测试中取得较高 MFU 和 MBU，并且性能 TCO 优于 NVIDIA GB300。 如果这些结论成立，Trainium3 可能为 AWS 客户提供比 NVIDIA Blackwell Ultra 成本更低、能效更高的推理选择，从而加剧 AI 加速器竞争并对 GPU 定价形成压力。 Trainium3 采用 3nm 制程，AWS 曾表示其算力约为 Trainium2 的两倍，能效提升 40%；对比对象 GB300 是 NVIDIA 的 Blackwell Ultra GPU，配备 288GB HBM3e 内存。SemiAnalysis 的分析强调基于第一性原理的物理架构和低延迟指标，但所提供的摘要未披露绝对基准数值。

rss · Semianalysis · 11月27日 15:54

**背景**: AWS Trainium 是亚马逊自研的 AI 加速器系列，旨在减少对 NVIDIA GPU 的依赖并降低云端 AI 工作负载的运行成本。推理是训练完成的模型对外提供预测的阶段，随着模型部署给数百万用户，其规模化成本敏感度越来越高。TCO 综合了硬件、电力、冷却和运维成本，而 MFU 与 MBU 衡量芯片理论算力和内存带宽的实际利用率。NVIDIA GB300 属于 Blackwell Ultra 代际，是高端 AI 数据中心系统的重要对标产品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://technews.tw/2024/12/05/aws-trainium3-ai-chip-powered-by-3-nanometers/">3 奈米加持 AWS Trainium 3 AI... | TechNews 科技新報</a></li>
<li><a href="https://grokipedia.com/page/NVIDIA_GB300">NVIDIA GB300</a></li>
<li><a href="https://inferencex.semianalysis.com/glossary/model-flops-utilization">What Is Model FLOPs Utilization (MFU)? | InferenceX</a></li>

</ul>
</details>

**标签**: `#AWS Trainium`, `#AI hardware`, `#inference`, `#microarchitecture`, `#NVIDIA`

---

<a id="item-7"></a>
## [Minecraft Java 版曝 Minecraft2Shell 远程代码执行漏洞，恶意资源包字体可入侵客户端](https://t.me/zaihuapd/45413) ⭐️ 8.0/10

11 月 22 日公开的 minecraft2shell 漏洞验证代码显示，攻击者通过服务器资源包下发特制的 TrueType 字体，即可触发 FreeType 2.14.3 及更早版本中的原生越界写，进而在 Windows 平台的 Minecraft Java 版客户端上执行任意代码。据报道，Java 版 1.20.5 至 1.21.10 以及 26.1 至 26.4 快照均受影响，而 1.20.4 及更早版本和基岩版不受影响。 由于利用该漏洞只需要玩家加入服务器并接受其资源包——这本来就是多人游戏的日常操作——几乎所有 Java 版玩家和公开服务器都处于风险之中，恶意服务器无需任何进一步交互即可入侵客户端电脑。这对服务器运营者、托管服务商和玩家社区都构成严重威胁，也再次说明打包进 Java 游戏的原生库可以绕过 JVM 通常提供的内存安全保护。 披露时 Mojang 仍在使用的 lwjgl-freetype 版本为 3.4.3，尚无补丁，而漏洞利用链位于 Minecraft 渲染文字所用的原生 FreeType 库中，因此 Java 层沙箱无法提供防护；社区追踪者称 Mojang 已于 11 月 24 日为 26.3 版本发布修复，玩家需完全关闭游戏并从启动器重新启动才能获取更新。需要注意的是，手动安装并启用恶意资源包同样可以触发该漏洞，因此风险并不限于加入服务器。

telegram · zaihuapd · 11月27日 18:04

**背景**: Minecraft 的资源包是可随服务器下发的资源集合，其中可以包含自定义字体，而游戏使用 FreeType 来渲染这些文字；FreeType 是一个广泛使用的开源字体光栅化库，以 C 语言编写，Java 端通过 LWJGL 绑定（lwjgl-freetype）调用。由于 FreeType 属于原生代码，字体解析中的内存安全缺陷——与编号 CVE-2025-27363 的 FreeType 越界写属于同一类问题——可以突破 JVM 的内存安全边界，使一个畸形字体文件变成代码执行的入口。这正是看似无害的外观类功能（如自定义字体）会演变为远程代码执行攻击面的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://liquidbounce.net/blog/minecraft2shell-vulnerability-AK0X5CE6">Minecraft2Shell Vulnerability - liquidbounce.net</a></li>
<li><a href="https://wurst.wiki/minecraft2shell">Minecraft2Shell Vulnerability - wurst.wiki</a></li>
<li><a href="https://seclists.org/oss-sec/2025/q1/205">oss-sec: CVE-2025-27363: out of bounds write in FreeType <= 2.13.0</a></li>

</ul>
</details>

**标签**: `#Minecraft`, `#RCE`, `#FreeType`, `#security vulnerability`, `#Java`

---