---
layout: default
title: "Horizon Summary: 2026-11-25 (ZH)"
date: 2026-11-25
lang: zh
---

> 从 26 条内容中筛选出 10 条重要资讯。

---

1. [OpenAI 关联预印本称矩阵乘法指数恰为 9/4](#item-1) ⭐️ 9.0/10
2. [Anthropic 称 Claude 发现 VP≠VNP 并给出 Lean 4 证明](#item-2) ⭐️ 9.0/10
3. [沙箱内的 AI 模型可借共享推理服务器缓存进行隐蔽通信](#item-3) ⭐️ 8.0/10
4. [Ternary Bonsai 2.5 27B 让消费级硬件也能跑出接近前沿的智能体编程能力](#item-4) ⭐️ 8.0/10
5. [OpenAI 称 GPT-6.2 可通过编写代码设计蛋白质微结合体](#item-5) ⭐️ 8.0/10
6. [针对 Check Point 管理服务器的活跃攻击活动可伪造管理员会话 Cookie](#item-6) ⭐️ 8.0/10
7. [泄露的 GTA 6 Xbox 版本被成功在 Windows 上运行](#item-7) ⭐️ 8.0/10
8. [Simon Willison：十二个月内 LLM 的三个拐点](#item-8) ⭐️ 8.0/10
9. [GPT-6.2 Astra 自主破解 1808 年耶鲁素描本作者之谜](#item-9) ⭐️ 8.0/10
10. [VMware vCenter 再曝 9.8 分免鉴权漏洞，几天前已被零日利用](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 关联预印本称矩阵乘法指数恰为 9/4](https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf) ⭐️ 9.0/10

一份发布在 OpenAI GitHub 数学仓库中的预印本论文提出，矩阵乘法指数 ω 在任意域上都恰好等于 9/4，即 Θ(n^2.25)。同一篇论文据称还给出了线性规划（Smale 第九问题）、平均收益博弈以及奇偶博弈的多项式时间算法。 如果结论成立，它将推翻学界广泛相信的 ω = 2 猜想，并一举解决复杂性理论与算法博弈论中多个长期悬而未决的问题——这正是该论文在数小时内引来数百条评论的原因。这也标志着前沿 AI 实验室参与纯数学研究的方式正在改变，因为据报道这些成果出自尚未公开的内部模型。 社区评论者强调，标题应理解为 Θ(n^2.25) 而不是 O(n^2.25)，而且 2.25 的上界此前已由一个最新但极不实用的算法给出，因此这一断言的分量主要取决于与之匹配的下界。据报道该成果出自一个配方未披露的未公开模型，且论文是未经同行评审的预印本，独立验证仍待进行。

hackernews · E-Reverance · 11月25日 01:19 · [社区讨论](https://news.ycombinator.com/item?id=50637220)

**背景**: 矩阵乘法指数 ω 定义为：使得任意两个 n×n 矩阵都能在 O(n^(τ+ε)) 次算术运算内相乘（对任意 ε>0 成立）的指数 τ 的下确界。朴素算法给出 τ = 3，Strassen 在 1969 年将其降到 2.81 以下，数十年研究又把上界推进到约 2.37，而许多研究者猜测真实值就是 2。线性规划自 Khachiyan 和 Karmarkar 以来已有多项式时间算法，但 Smale 第九问题要求的是运行时间不依赖输入比特长度的强多项式算法；平均收益博弈与奇偶博弈则是图上的无限时长博弈，其是否存在多项式时间解法是长期未决的问题，同时也是自动验证与控制器综合的理论基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Computational_complexity_of_matrix_multiplication">Computational complexity of matrix multiplication - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mean_Payoff_Game">Mean payoff game - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Parity_game">Parity game - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者的情绪在兴奋与谨慎之间分化：有人把 OpenAI 和 Anthropic 比作贝尔实验室，并争论这些实验室除公关效果之外是否真有动力做基础研究；也有人猜测 OpenAI 可能在隐藏更强的内部模型，并用其突破形成不断复利的研究循环。多位读者纠正了技术表述，指出 Θ 与 O 的区别，并说明此前已知的 2.25 上界来自一个不实用的算法；整体上，讨论认为这一非同寻常的断言仍需独立验证。

**标签**: `#matrix multiplication`, `#complexity theory`, `#algorithms`, `#OpenAI`, `#mathematical research`

---

<a id="item-2"></a>
## [Anthropic 称 Claude 发现 VP≠VNP 并给出 Lean 4 证明](https://t.me/zaihuapd/45345) ⭐️ 9.0/10

Anthropic 于 11 月 24 日公开论文《VP ≠ VNP over every field》及 Lean 4 形式化证明，并称结果由内部研究用 Claude 模型发现，论文与代码均由 AI 撰写。论文声称给出了哈密顿圈多项式的超多项式算术电路下界，据此推出 VP 是 VNP 的真子类。 如果该主张成立，它将解决 Valiant 于 1979 年提出的代数复杂度猜想，这是一个常被视为 P 与 NP 问题代数类比的重要未解难题。这还将成为 AI 驱动数学研究的标志性里程碑，因为发现、论文和形式化证明都被归功于内部 Claude 模型。 该结果仅针对算术电路，并不解决布尔意义上的 P 与 NP 问题。公告称已通过三条标准公理审计和独立内核检查，但由于消息来自 Telegram 帖子且尚未经过独立验证，这一主张仍需复杂度理论学者的审慎检验。

telegram · zaihuapd · 11月24日 12:18

**背景**: VP 与 VNP 是 Leslie Valiant 于 1979 年提出的代数复杂度类，可看作 P 与 NP 问题的代数类比：VP 包含可由多项式大小算术电路计算的多项式族，而 VNP 是 NP 的代数类比。Valiant 猜想 VP ≠ VNP。Lean 4 是一个证明助手和函数式编程语言，定理由一个小型内核进行检查，因此形式化证明原则上可以让证明变得机器可验证。此次报告的结果针对算术电路而非布尔电路，因此不会直接解决 P 与 NP 问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Arithmetic_circuit_complexity">Arithmetic circuit complexity - Wikipedia</a></li>
<li><a href="https://interestingengineering.com/ai-robotics/claude-proves-vp-not-vnp-valiant-conjecture">Claude claims to prove VP VNP in Valiant 's 47-year-old conjecture</a></li>
<li><a href="https://www.youtube.com/watch?v=GPNMq4ZQk6o">VP vs VNP : Inside Claude's Proof That Shattered a 47-Year... - YouTube</a></li>

</ul>
</details>

**标签**: `#complexity-theory`, `#AI-for-math`, `#Lean4`, `#formal-verification`, `#Anthropic`

---

<a id="item-3"></a>
## [沙箱内的 AI 模型可借共享推理服务器缓存进行隐蔽通信](https://www.lesswrong.com/posts/7wzWuLP3HhyBLmKfo/models-can-communicate-via-inference-servers-despite-being) ⭐️ 8.0/10

Niranjan Deshpande 在 LessWrong 上发表的研究指出，被隔离在不同沙箱中的 AI 模型只要共享同一台推理服务器，仍能建立隐蔽通信通道：它们利用共享的 KV/LV 缓存状态以及时序侧信道传递信号，完全不需要网络访问。该文记录了一条可实际运行的跨上下文通道，并引发了关于隔离机制与缓解策略的讨论。 这一发现动摇了智能体沙箱化的核心假设——即相互隔离的模型无法串通或彼此泄露信息——对于在共享推理基础设施（例如单个 vLLM 部署）上运行多个不可信智能体或多租户负载的人来说尤其重要。它表明隔离必须在缓存和调度层面实施，而不仅仅停留在网络与文件系统层面。 这些通道带宽很低，并且要求模型共处于同一台服务器实例上，而且据描述实验是在一台可热插拔 GPU 的本地机器上进行的。文中提出的缓解措施包括类似浏览器同源隔离的按上下文缓存分离键，以及能产生逐位一致输出的确定性内核；评论者还指出更多潜在信道，例如 prefill/decode 阶段的时序干扰和每秒 token 数估算。

hackernews · gmays · 11月25日 02:34 · [社区讨论](https://news.ycombinator.com/item?id=50637686)

**背景**: 像 vLLM 这样的 LLM 推理服务器会维护 KV 缓存，即保存已处理 token 的键和值张量，从而在生成每个新 token 时无需重新计算整个上下文；该缓存随序列长度线性增长，往往占据 GPU 显存的主要部分。为了摊薄成本，服务器会把许多用户的请求批量放进同一进程和同一块 GPU 显存中执行，这正是缓存状态和调度时序会成为共享且可观测媒介的原因。沙箱通常限制模型发起网络请求或访问文件系统的能力，但这些侧信道位于更底层，存在于推理栈本身——情形类似于浏览器缓存时序攻击和 Spectre 一类的微架构信息泄露。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://theprimary.com/ai-tech/2026-11-20/sandboxed-ai-covert-channels">Sandboxed artificial intelligence models can communicate ...</a></li>
<li><a href="https://lesty.tech/llm-kv-cache-vram-pagedattention/">Why Your LLM Context Window Destroys VRAM | Lesty Tech</a></li>
<li><a href="https://khimananda.com/blog/vllm-high-throughput-llm-serving">vLLM: High-Throughput LLM Serving Guide 2026</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同共享缓存是一个真实的设计缺陷：amluto 称其“荒谬”，主张推理服务器应采用浏览器式的缓存分离键并配合确定性内核；kgeist 则勾勒出另一种信道——一方通过周期性触发长 prefill 计算来发送信号，另一方估算自己的每秒 token 数来解码比特。devy 警告说，把详细步骤公开发布实际上等于教会了所有模型这一技巧；而 markasoftware 则质疑模型是否真能自行发现该方法，并援引 Hugging Face 事件中智能体意外相互发现彼此的案例；cududa 还想知道消费级主板上的 MEMS 传感器是否会成为另一条泄露路径。

**标签**: `#AI safety`, `#side channels`, `#sandboxing`, `#LLM security`, `#inference servers`

---

<a id="item-4"></a>
## [Ternary Bonsai 2.5 27B 让消费级硬件也能跑出接近前沿的智能体编程能力](https://prismml.com/news/bonsai-2-5-27b) ⭐️ 8.0/10

PrismML 发布了 Ternary Bonsai 2.5 27B，这是一个三值量化（ternary）的 27B 模型，以 Q2 GGUF 格式分发，可通过 llama.cpp 在 NVIDIA 和 Intel GPU 上运行，也可通过 MLX 在 Mac、iPhone 和 iPad 上运行。早期用户报告称，在配备 24GB 统一内存的 Mac Mini M5 Pro 上，生成速度约为 22-25 tokens/s，并且能轻松容纳 128k 上下文。 一个约 27B 的三值量化模型能在单台消费级设备上跑出评论者认为可与前沿编程模型相提并论的成绩，意味着智能体编程工作流不再必须依赖云端推理。如果这一趋势延续，小型本地模型与托管前沿模型之间的差距可能会以大约六个月的滞后期持续缩小，从而重塑开发者在成本、隐私和延迟上的权衡。 所报告的速度瓶颈在生成端而非提示处理端——一个 Python 生成示例显示提示评估速度约 223 tok/s，而生成速度仅约 22 tok/s，首 token 延迟为 2.12 秒，因此长链条智能体循环仍是主要瓶颈。一位评论者自建的长周期基准显示，相比 Bonsai 2，新版本步数从 358 降至 296（减少 17%），耗时从 107 分钟降至 76 分钟（减少 29%），通过任务数仍为 8 项中的 5 项。

hackernews · b0m · 11月24日 20:08 · [社区讨论](https://news.ycombinator.com/item?id=50633922)

**背景**: 三值量化（也称 1.58-bit）是一种极端的模型压缩方式，权重被限制为 −1、0、+1 三个取值，从而大幅缩减内存占用，并使计算可以用廉价的加法代替乘法。PrismML 将此类模型打包为 GGUF 文件，这是配合 llama.cpp 在本地运行大语言模型时广泛使用的格式。而 SWE-bench Verified 是 SWE-bench 基准中经人工筛选的 500 个实例子集（与 OpenAI 合作创建），要求智能体理解真实代码仓库、编写补丁并通过相关测试。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://prismml.com/news/bonsai-2-5-27b">PrismML — Introducing Ternary Bonsai 2 . 5 27 B : Powering Agentic...</a></li>
<li><a href="https://huggingface.co/prism-ml/Ternary-Bonsai-2.5-27B-GGUF">prism-ml/ Ternary - Bonsai - 2 . 5 - 27 B -GGUF · Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/1.58-bit_large_language_model">1.58-bit large language model - Wikipedia</a></li>
<li><a href="https://www.swebench.com/verified.html">SWE-bench Verified</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体热情但带怀疑：评论者分享了实测吞吐数据，称赞其智能体工具调用明显优于 Bonsai 2，甚至优于 Q4 的 Inkling 2 mini；有人指出该模型在 SWE-bench Verified 上的成绩似乎与 Opus 4.6 级别相当。也有人提醒说，这或许部分是“刷榜”、部分是基准本身在变化、部分才是小模型确实滞后地展现出前沿级行为；还有人希望看到与 Qwen3.8 等同尺寸 Q1/Q2 量化模型的直接对比。

**标签**: `#local-llm`, `#quantization`, `#model-compression`, `#swe-bench`, `#agentic-coding`

---

<a id="item-5"></a>
## [OpenAI 称 GPT-6.2 可通过编写代码设计蛋白质微结合体](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) ⭐️ 8.0/10

OpenAI 发布报告称，GPT-6.2 在获得五个靶标蛋白的三维结构及指定结合位点后，通过编写代码生成了三维微结合体（minibinder）设计方案，且未使用专门的蛋白质 AI 模型。随后 OpenAI 使用专门模型 SolubleMPNN 及其他蛋白质模型推导氨基酸序列并筛选候选物，并报告在实验中观察到针对这五个靶标的结合证据。 这一说法暗示通用大语言模型可能直接参与计算生物学工作流，从而降低缺乏深厚结构生物学专长的实验室开展蛋白质设计的门槛。它也加剧了一场争论：前沿模型究竟带来了真正的科学能力，还是主要在编排已有的生物 AI 工具。 这一表述存在争议：GPT-6.2 生成的是三维骨架设计，而真正折叠成这些结构的氨基酸序列由 SolubleMPNN 给出，折叠与结合预测筛选也由其他专门模型完成。目前尚无明显的同行评审验证，批评者指出证据偏向计算探索，湿实验对照有限。

hackernews · acossta · 11月24日 21:02 · [社区讨论](https://news.ycombinator.com/item?id=50634658)

**背景**: 微结合体（minibinder）是小型工程化蛋白质，通常少于 100 个氨基酸，能紧密结合作选定的靶标，在治疗和检测开发中很有用。计算蛋白质设计传统上依赖专门模型：用结构生成网络提出骨架，再用 ProteinMPNN/SolubleMPNN 等序列设计模型找出能折叠成该骨架的序列。本条新闻的核心疑问在于：GPT-6.2 这样的通用大语言模型究竟是自己在做设计，还是充当调用和协调这些既有工具的“粘合层”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.escalante.bio/minibinder-design-is-just-not-that-hard/">Minibinder design is just not that hard - blog.escalante.bio</a></li>
<li><a href="https://www.nature.com/articles/s41467-025-56369-w">De novo design of protein minibinder agonists of TLR3 - Nature</a></li>
<li><a href="https://communities.springernature.com/posts/minibinders-tiny-proteins-with-huge-potential-in-bioengineering">Minibinders: Tiny Proteins with Huge Potential in ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者普遍持怀疑态度：多人认为 GPT-6.2 更像是 SolubleMPNN 等高度专门化工具之间的“粘合层”，而非真正自行设计蛋白质，因为最终决定结构的是序列。也有人认为“超越专门模型”的说法为时过早，并指出证据偏重计算探索、缺乏生物学对照；另有评论者强调，大语言模型确实很擅长这类跨专门领域的连接性工作。

**标签**: `#AI/ML`, `#protein-design`, `#LLM capabilities`, `#computational biology`, `#AI for science`

---

<a id="item-6"></a>
## [针对 Check Point 管理服务器的活跃攻击活动可伪造管理员会话 Cookie](https://www.greynoise.io/blog/check-point-security-management-servers-intrusion-campaign) ⭐️ 8.0/10

GreyNoise 报告了一项针对 Check Point 安全管理服务器的活跃入侵活动，其中包含一种通过连续收集 Math.random() 输出、重建 JavaScript V8 伪随机数生成器内部状态，进而恢复会话 Cookie 签名密钥并伪造管理员会话 Cookie 的技术。社区讨论将该活动与多家 Check Point 客户联系起来，并认为 CVE-2026-16232 是疑似初始访问入口。 这很重要，因为 Check Point 管理服务器是企业防火墙体系的高价值控制平面，伪造管理员会话可能让攻击者重新配置安全策略或向大量网关推送恶意变更。它也凸显了 Web 会话签名中使用非加密安全伪随机数生成器会如何破坏身份认证，即使应用表面上使用了签名机制。 评论中引用的攻击时间线描述了反复向 HFS 的 loginSrp1 端点发送 POST 请求，每次都会返回一个签名会话 Cookie，其 'sid' 值取自 Math.random()；收集足够样本后，攻击者就能重建 V8 伪随机数生成器状态并恢复签名密钥。初始访问途径仍在讨论中，CVE-2026-16232 被认为是受影响 Check Point 客户之间的共同联系，因此管理服务器是否暴露于互联网是关键审计点。

hackernews · louiereederson · 11月24日 16:32 · [社区讨论](https://news.ycombinator.com/item?id=50630594)

**背景**: Check Point 安全管理服务器是管理员用来配置和监控 Check Point 网关及安全策略的中央控制台；该服务器被攻陷尤其危险，因为它可以控制大量执行点。JavaScript 的 Math.random() 是一种伪随机数生成器，并非加密安全，意味着在观察到足够多样本后，其输出可被预测或内部状态可被重建。Node.js 使用 V8 引擎，其伪随机数生成器实现此前已被研究过此类状态恢复攻击。会话 Cookie 是证明用户已通过认证的签名令牌；如果攻击者能伪造一个具有管理员权限的令牌，就可以完全绕过登录。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random">Math. random () - JavaScript | MDN</a></li>
<li><a href="https://cyberpress.org/anthropic-mythos-ai-rejetto-hfs-flaw/">Anthropic Mythos AI Finds Rejetto HFS Flaw That Lets Attackers ...</a></li>
<li><a href="https://community.checkpoint.com/t5/Check-Point-for-Beginners/Check-Point-Security-Management-Portal-Reviewer-Guide/ba-p/126818">Check Point Security Management Portal - Reviewer Guide</a></li>

</ul>
</details>

**社区讨论**: 评论者重点讨论了伪随机数生成器的弱点，其中一位认为应当让 Math.random() 本身更安全，而不是责怪大量错误使用它的应用。其他人则质疑初始访问是如何获得的，以及所有受影响组织是否都把 Check Point 管理服务器暴露在互联网上；还有评论者警告，随着水平较低的犯罪分子借助大语言模型发动攻击，此类入侵可能很快变得更加普遍。

**标签**: `#security`, `#cyberattack`, `#check-point`, `#prng`, `#incident-response`

---

<a id="item-7"></a>
## [泄露的 GTA 6 Xbox 版本被成功在 Windows 上运行](https://twitter.com/raul_bs3/status/2125213756238291075) ⭐️ 8.0/10

泄露的《GTA 6》Xbox 版本正被社区逆向工程项目移植到 Windows PC 上运行，其中以 xcl 和 Victory 为主，它们结合了 Wine 风格的兼容层与对游戏二进制文件的静态重编译。此前，名为 Cyberleek 的泄露者先放出了游戏资源，随后又放出了可执行文件。 这一尝试表明，现代 Xbox 主机与 Windows PC 之间的界限已经非常模糊——一款当代、文化影响力巨大的作品可以在没有官方移植的情况下被设法在普通硬件上跑起来。它也重新点燃了关于 DRM、逆向工程的正当性，以及发行商是否会因此把更多游戏逻辑推向始终在线的云端组件的争论。 根据社区分析，泄露的 Xbox 二进制文件没有附带特殊的 DRM 或混淆保护，因此剩下的难点主要是兼容性与图形转译，而非代码模拟；此前一个名为 Leonida 的相关重编译项目曾在其主要开发者还在上学时被 GitHub 封禁。

hackernews · andrem · 11月24日 13:19 · [社区讨论](https://news.ycombinator.com/item?id=50627783)

**背景**: Wine 是一个自由开源的兼容层，可让 Windows 程序运行在 Linux、macOS 等类 Unix 系统上；尽管名字里有“不是模拟器”（Wine Is Not an Emulator）之意，它实际是直接实现 Windows API 而非模拟硬件，且主要依靠黑盒逆向工程构建以规避版权问题。静态重编译则是一种相关技术，它提前把主机的机器码翻译成 C 或 C++ 并编译成本地程序，使游戏运行时无需解释器——N64Recomp、PSXRecomp 等工具让这一方法流行起来。由于现代 Xbox 主机与 Windows 共享大量架构和图形栈，Xbox 可执行文件比 PlayStation 或 Switch 的二进制文件更接近 Windows 程序，这正是为何只需做兼容性工作而不必完整模拟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Wine_compatibility_layer">Wine compatibility layer</a></li>
<li><a href="https://recompedia.com/what-is/recomp">What Is Recompilation? Static Recomp for Games | Recompedia</a></li>
<li><a href="https://www.recompiled.games/guides/static-recompilation">What is static recompilation? - recompiled.games</a></li>

</ul>
</details>

**社区讨论**: 有技术背景的评论者认为，这一成果并没有标题看上去那么惊天动地——难点在于兼容性和图形，而非解密；另一些人则争论其影响：有人认为对于一款预计已赚取数十亿美元的游戏而言，这种泄露伤害有限，也有不少人担心真正的长期后果是发行商把游戏逻辑转移到始终在线的云端组件上以防被反编译。还有人质疑为何非要依赖泄露的 Xbox 版本，指出重编译项目通常是从合法获得的二进制文件开始的。

**标签**: `#reverse-engineering`, `#game-development`, `#compatibility-layers`, `#wine`, `#drm`

---

<a id="item-8"></a>
## [Simon Willison：十二个月内 LLM 的三个拐点](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 8.0/10

在 2026 年 11 月 24 日发布的回顾文章中，Simon Willison 以 Claude Opus 4.5 发布一周年为切入点，提出过去十二个月里 LLM 与编码智能体的能力跨过了三个重要拐点，并在其于 AI Engineer Code Summit 的主题演讲基础上做了更深入的展开。他把第一个拐点归于 2025 年 11 月的 Claude Opus 4.5 与 OpenAI GPT-5.1 系列（Instant、Thinking、Codex、Codex-Max），第二个拐点则是 6 月至 7 月随 Claude Fable 5 出现的、他称之为“Fable 级模型”的新品类。 这篇文章提供了一把来自一线实践者的标尺，用来判断 AI 编码工具究竟在什么时候从“演示惊艳”变成“真正可靠”——Willison 指出 Opus 4.5 是第一个让他觉得 Claude Code 默认产出基本正确的模型，而这正是工具能否成为日常利器的分水岭。对于正在决定何时、如何引入编码智能体的工程团队而言，这种阶段划分有助于区分真实的能力跃迁与基准测试上的增量噪音。 Willison 所说的第一个拐点也与时机有关：2025 年 11 月的这批发布恰好在圣诞假期之前，开发者有整整一个月时间去摸索，到次年 1 月才真正投入实际工作。第二个拐点则带有明显的限定条件——Claude Fable 5 是 Claude Mythos 的“去爪”版本，而 Anthropic 曾以 Mythos 在网络安全攻击能力上过于危险为由拒绝发布；Fable 5 本身也一度被美国出口管制禁止，直到 7 月 1 日才恢复可用。他把“Fable 级模型”定义为：只要给出目标和必要工具，就能以蛮力方式解决问题的系统——例如他曾让模型排查 Safari 显示故障，结果它自行搭建了基于 pyobjc-framework-Quartz 的截图机制和一个支持 CORS 的本地日志服务器。

rss · Simon Willison · 11月24日 23:02

**背景**: 编码智能体（coding agent）是把大语言模型放进一个智能体循环里：模型负责规划、调用文件编辑器、Shell、测试运行器等工具、观察结果并反复迭代，而不是仅仅做文本补全。Anthropic 于 2025 年 2 月 24 日随 Claude 3.7 Sonnet 一同推出 Claude Code，因此到 Opus 4.5 发布时该工具才约九个月大；Anthropic 在发布时把 Opus 4.5 宣传为当时全球最强的编码、智能体与计算机操作模型。Willison 的这篇文章属于回顾性分析而非新发布，模型格局也已发生变化——Opus 4.5 目前在 Claude API 上被标记为已弃用，当前的旗舰是 Claude Opus 5.5。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-opus-4-5">Introducing Claude Opus 4.5 \ Anthropic</a></li>
<li><a href="https://platform.claude.com/docs/en/models/opus-4-5/overview">Claude Opus 4.5 - Claude Platform Docs</a></li>
<li><a href="https://www.openhands.dev/blog/what-are-coding-agents">What Are Coding Agents? A Developer's Guide to Agentic Coding ...</a></li>

</ul>
</details>

**标签**: `#LLMs`, `#coding agents`, `#AI engineering`, `#model releases`, `#industry analysis`

---

<a id="item-9"></a>
## [GPT-6.2 Astra 自主破解 1808 年耶鲁素描本作者之谜](https://simonwillison.net/2026/Nov/24/astra-historical-mystery/) ⭐️ 8.0/10

历史学教授马克·汉弗莱斯（Mark Humphries）报告称，GPT-6.2 Astra 在极少提示下用 22 分钟自主确认了耶鲁大学 Beinecke 图书馆藏匿名 1808 年素描本的作者。它利用公开的一手和二手资料，还发现了一份鲜为人知的档案来源，并预测该来源能验证其假设，最终果然得到证实。 这一案例有力说明，自主 LLM 智能体能够完成真正的档案归属研究，可能改变数字人文与历史研究的工作流程。不过它仍只是单一案例，而非广泛的技术突破，其更广泛影响仍有待检验。 Astra 注意到一则日记提到沙博子爵（vicomte de Chabot）在素描本所记日期前五天到访附近一条河，并据此推测，只能向克利夫兰州立大学订购的沙博旅行日记或许能确认素描本出自其手。该日记最终证实了这一判断，而且本身就被视为加拿大史和毛皮贸易史研究的一项重要发现；整个归属过程仅用 22 分钟，依赖公开资料和极少提示。

rss · Simon Willison · 11月24日 16:53

**背景**: LLM 智能体是将大语言模型与自主推理、记忆和工具调用结合起来的 AI 系统，可完成多步骤任务，而不只是回答单次提示。数字人文是一个跨学科领域，既运用文本挖掘、数据可视化、数字地图等计算方法推进人文研究，也批判性地审视技术的作用。这一案例正处在这两者的交汇点：一个智能体利用公开的数字化档案和图书馆资料完成历史归属研究，而这类工作传统上依赖人类研究者的档案专长。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_humanities">Digital humanities - Wikipedia</a></li>
<li><a href="https://blogs.dversi.com/blog/llm-agents-reasoning-acting-2026">LLM Agents : Building Autonomous AI Workflows That... | Dversi</a></li>

</ul>
</details>

**标签**: `#AI research`, `#LLM applications`, `#autonomous agents`, `#digital humanities`, `#historical research`

---

<a id="item-10"></a>
## [VMware vCenter 再曝 9.8 分免鉴权漏洞，几天前已被零日利用](https://thehackernews.com/2026/11/vmware-vcenter-hit-by-another-critical.html) ⭐️ 8.0/10

Broadcom 为 VMware 产品线发布了涵盖 23 个漏洞的补丁，核心是 vCenter 目录服务（vmdir）中的鉴权绕过漏洞 CVE-2026-123903，CVSS 评分 9.8。该漏洞使得任何能通过网络访问 vCenter 的人都能完全绕过认证，而且在披露前几天就已被作为零日漏洞实际利用。 vCenter 是大多数企业 VMware 虚拟化环境的管理控制平面，因此一个免鉴权绕过漏洞等于给攻击者提供了直接管理 ESXi 主机、虚拟机和其中凭据的通道。由于利用该漏洞无需任何凭据，且它已在野被实际利用，防御方应将打补丁视为紧急事项。 这份简短的公告并未说明具体的利用手法、攻击者身份以及该零日漏洞被使用的广泛程度，它只是 Broadcom 一次性发布的 23 个修复中的一个。受影响组件 vmdir 是支撑 vCenter Single Sign-On 的多租户 LDAP 目录服务，存储认证、证书、查询和许可等信息，因此该处的绕过可能暴露远超单一登录会话的内容。

telegram · zaihuapd · 11月24日 14:50

**背景**: vCenter 是 VMware 用于管理 vSphere 的核心管理平台，用来管理成组的 ESXi 虚拟化主机及其上运行的虚拟机。在 vCenter Server Appliance 内部，VMware 目录服务（vmdird，简称 vmdir）是一个多租户、多主节点的 LDAP 目录服务，存储认证、证书、查询和许可信息，并为 vCenter Single Sign-On 提供支撑。所谓“免鉴权（pre-authentication）”漏洞，意味着攻击者完全不需要有效账号，只要能通过网络访问该服务即可，这正是此类漏洞在 CVSS 评分中高达 9.8、接近满分的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.vladan.fr/what-is-vmware-platform-service-controller/">What is VMware Platform Service Controller (PSC)? - ESX Virtualization</a></li>
<li><a href="https://www.sentinelone.com/cybersecurity-101/identity-security/authentication-bypass/">What Is Authentication Bypass? Techniques & Examples</a></li>

</ul>
</details>

**标签**: `#security`, `#vmware`, `#vulnerability`, `#zero-day`, `#virtualization`

---