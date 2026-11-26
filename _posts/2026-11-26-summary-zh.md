---
layout: default
title: "Horizon Summary: 2026-11-26 (ZH)"
date: 2026-11-26
lang: zh
---

> 从 34 条内容中筛选出 8 条重要资讯。

---

1. [斯科特·阿伦森回应「矩阵乘法指数恰为 9/4」的宣称](#item-1) ⭐️ 9.0/10
2. [Anthropic 的 1700 万行 GRH Lean 证明被压缩至 7.6 万行](#item-2) ⭐️ 9.0/10
3. [1Password 披露安全事件：员工设备被入侵后代码被推向后端服务](#item-3) ⭐️ 8.0/10
4. [Google Research 发布关于整数分解与离散对数的“Cogentic”系列论文](#item-4) ⭐️ 8.0/10
5. [开发者用 Lean 审计 Clojure 核心库，发现未报告缺陷](#item-5) ⭐️ 8.0/10
6. [美国出台新规，堵住远程调用先进 AI 芯片的漏洞](#item-6) ⭐️ 8.0/10
7. [Minecraft Java 版 1.20.5 起全版本受高危 RCE 漏洞影响，恶意字体可远程执行代码](#item-7) ⭐️ 8.0/10
8. [三星电子与 SK 海力士据称将通过交叉许可采用长江存储 Xtacking 技术](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [斯科特·阿伦森回应「矩阵乘法指数恰为 9/4」的宣称](https://scottaaronson.blog/?p=10379) ⭐️ 9.0/10

斯科特·阿伦森（Scott Aaronson）发表了题为《Holy shit holy shit holy shit holy shit: The magnitude of what's now happening》的博文，回应 OpenAI 于 11 月 24 日发布的一篇预印本——该文宣称方阵乘法的指数 ω 在任意域上都恰好等于 9/4，并附有覆盖「无除法情形」的 Lean 形式化证明。这篇博文引来一千多条评论，成为当周讨论最热烈的技术话题之一。 如果这一宣称成立，它将为一个悬而未决数十年的代数复杂度难题画上句号：为 OpenAI 自己在 10 月公布的快速矩阵乘法上界补上相匹配的下界，其影响会波及算法设计与复杂度理论。更关键的是，这一证明据称出自一家 AI 实验室而非人类数学家之手，这使一个原本小众的定理演变成一场更广泛的争论：AI 的数学能力究竟能推广多远——用阿伦森的话说，还有哪些被认为「难解」的问题会接连倒下。 该预印本没有署名任何个人作者，也没有指明使用了哪个模型，而且其 Lean 形式化只覆盖了无除法情形，因此关于任意域的完整结论依赖的是文字论证而非机器检验的证明。作为参照：多年来已知最好上界一路下探到大约 ω < 2.37，而普适下界始终只有平凡的下界 2，这正是「下界为 2.25」这一半宣称最令人震惊的原因。

hackernews · Kotlopou · 11月25日 19:11 · [社区讨论](https://news.ycombinator.com/item?id=50646108)

**背景**: 矩阵乘法指数 ω 的定义是：使两个 n×n 矩阵能够在 O(n^(τ+ε)) 次算术运算内相乘（对任意 ε > 0）的所有指数 τ 的下确界；朴素算法对应 τ = 3，而斯特拉森（Strassen）1969 年的结果首次将其压到 3 以下。由于下界 2 是平凡的（任何算法至少要读完输入），真正有意思的问题是真实值落在 2 与已知最好上界之间的什么位置——精确确定它，就等于确定了计算领域最基础运算之一的渐近复杂度。阿伦森的博文还延伸到密码学：公钥体系建立在被假定为真正困难的问题之上，因此「AI 能在一个长期悬而未决的困难性问题上取得突破」这一展示，自然引出「正在使用的密码是否仍然安全」的疑问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aitoolsrecap.com/Blog/openai-matrix-multiplication-exponent-nine-fourths">OpenAI Says Matrix Multiplication Stops at 9/4 | AIToolsRecap</a></li>
<li><a href="https://en.wikipedia.org/wiki/Computational_complexity_of_matrix_multiplication">Computational complexity of matrix multiplication - Wikipedia</a></li>
<li><a href="https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf">math/preprints/The-matrix-multiplication-exponent-is-nine ...</a></li>

</ul>
</details>

**社区讨论**: 评论者大致分为几派：一派认为大型 AI 实验室目前几乎肯定没有可用的密码破解能力，因为这种规模的机构难免走漏消息，如此重大的突破必然会有吹哨人或泄密者出现。另一派则质疑「外推」本身，指出 AI 在公理化的先验数学上很强，并不意味着它能「解决」经验性学科，更不意味着它会扮演科幻式的毁灭人类角色。还有一类是元层面的讨论：有评论者认为人类在生物学上根本无法感知到应有警报程度的哪怕一小部分，也有人援引布鲁诺·拉图尔（Bruno Latour）的「计算中心」概念与第谷·布拉赫整理天文数据的工作，认为真正催生科学革命的往往是把知识组织起来，而非单纯的证明能力。

**标签**: `#AI`, `#cryptography`, `#mathematics`, `#algorithms`, `#research-breakthroughs`

---

<a id="item-2"></a>
## [Anthropic 的 1700 万行 GRH Lean 证明被压缩至 7.6 万行](https://github.com/lsernau/grh-lean) ⭐️ 9.0/10

开发者 lsernau 在 GitHub 上发布了 grh-lean 项目，对 Anthropic 关于广义黎曼假设（GRH）相关内容的 Lean 形式化进行了大幅压缩并补充人工文档，把这份由 AI 生成的证明从约 1700 万行削减到约 7.6 万行，压缩幅度达 99.56%。该仓库还把整个开发清晰地划分为“已知数学”与“新数学”两部分，并在各处补充了便于人阅读的说明文档。 这一结果直接回应了陶哲轩（Terence Tao）近期的批评：机器生成的形式化证明即便正确，也往往体量庞大、难以理解，无法给人带来洞察。如果庞大的 AI 证明能够被压缩数个数量级并配上文档，那么形式化验证作为 AI 生成数学与代码的“信任层”就更具可行性。 除了行数上的削减，该仓库的主要价值在于结构：把已有定论的结果与新形式化的内容分开，并用人类可读的文字为代码加注。需要警惕的是，7.6 万行策略式（tactic）Lean 代码仍远超任何人能逐行核对的规模，因此真正的可信性依然依赖 Lean 那个小巧的可信内核，而不是靠人去通读。

hackernews · nb-t · 11月25日 21:48 · [社区讨论](https://news.ycombinator.com/item?id=50648050)

**背景**: Lean 是一个开源的证明助手，它的每一步证明都由一个小巧的可信内核检查，因此即便没有人通读，形式化证明也能由机器验证其正确性。广义黎曼假设（GRH）把关于 zeta 函数零点的经典黎曼假设推广到更广泛的一类 L 函数（例如 Dirichlet L 函数），是解析数论中最核心的未解猜想之一。Anthropic 围绕 GRH 相关内容做出了一个规模极其庞大的 Lean 开发，而本项目是对这项工作的压缩与人工整理式重述，并非对该猜想本身给出了新证明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://agentconn.com/blog/verification-bottleneck-lean-trust-layer/">Lean Is Becoming AI 's Trust Layer - AgentConn Blog</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者称赞了“已知数学”与“新数学”的清晰划分以及随处可见的文档，认为这大大降低了理解难度。也有人质疑：让大模型去“打高尔夫式”压缩证明，究竟是真的回应了陶哲轩关于“缺乏洞察”的批评，还是只是造出了一个更小的不透明对象；还有不懂 Lean 的怀疑者看了代码样例后追问，现实中人类究竟有多可能读懂这些 Lean 代码并确认其正确性。

**标签**: `#formal-verification`, `#lean`, `#ai-for-math`, `#proof-compression`, `#riemann-hypothesis`

---

<a id="item-3"></a>
## [1Password 披露安全事件：员工设备被入侵后代码被推向后端服务](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

1Password 发布了关于 2026 年 11 月一起安全事件的更新说明：一名员工的设备被入侵，攻击者借此将恶意代码推向后端服务。官方公告描述了事件经过并列出补救措施，但并未说明是否启用了 GitHub 分支保护规则，也未说明这些规则是否被绕过。 1Password 是被广泛使用的密码管理器，任何“代码可能进入生产服务”的迹象都会让数以百万计把它当作安全边界的用户产生信任疑虑。这起事件也再次印证了行业的普遍规律：员工笔记本电脑被攻陷，如今已成为 SaaS 供应链最常见的入侵入口，所有拥有高权限开发者账户的公司都面临同样风险。 公告没有披露相关代码仓库是否配置了分支保护规则、强制 Pull Request 审核或必需的状态检查，而这正是“代码如何抵达生产环境”的关键未解问题。1Password 表示只有极少数用户处于受影响状态并已逐一通知，同时强调其端到端加密的保险库数据仍受底层加密设计保护。

hackernews · lxhrstn · 11月25日 17:18 · [社区讨论](https://news.ycombinator.com/item?id=50644817)

**背景**: GitHub 的分支保护规则允许仓库管理者禁止对 main 等重要分支进行强制推送和删除，并要求合并前必须获得审核批准或通过 CI 检查。当攻击者控制了开发者的笔记本电脑，就等于继承了该开发者的凭据，可以直接尝试推送代码，因此这些防护措施是“被钓鱼的终端”与“生产环境”之间的最后一道防线。SaaS 供应链攻击正是沿着这条路径展开：攻击者不直接篡改软件包，而是攻陷拥有部署权限的身份或设备，这也是为什么身份与终端的可见性和代码审查同样重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches">About protected branches - GitHub Docs</a></li>
<li><a href="https://www-theregister-com.nproxy.org/security/2026/05/15/openai-caught-in-tanstack-npm-supply-chain-chaos-after-employee-devices-compromised/5241019">OpenAI caught in TanStack npm supply chain chaos after employee ...</a></li>
<li><a href="https://appomni.com/blog/saas-supply-chain-attacks-mitre-attck-mapping/">SaaS Supply Chain Attacks : MITRE ATT&CK | AppOmni</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者整体上对公告的疏漏持批评态度，而非因此感到安心。安全专家 tptacek 认为“员工笔记本被入侵导致代码被推送”是 SaaS 公司最重要的攻击面，并指出随着员工人数增加，至少有一台笔记本被攻陷的概率趋近于 1；其他人则追问是否禁用了直接推送 main 分支、是否存在分支保护规则，还有用户称收到了一封疑似基于此次事件数据打造的高质量钓鱼邮件。

**标签**: `#security`, `#supply-chain`, `#saas`, `#password-managers`, `#incident-response`

---

<a id="item-4"></a>
## [Google Research 发布关于整数分解与离散对数的“Cogentic”系列论文](https://github.com/google-research/google-research/tree/master/cogentic_research_papers) ⭐️ 8.0/10

Google Research 在其 google-research 的 GitHub 仓库中发布了一批名为“Cogentic”的研究论文，内容涵盖整数分解、离散对数以及相关的计算数论问题。该发布在 Hacker News 上引发了热烈讨论（约 481 分、345 条评论），争论的焦点集中在这些结果的密码学意义上。 整数分解与离散对数正是 RSA、Diffie-Hellman 和 ElGamal 所依赖的困难性假设，因此任何声称在这两个问题上取得算法进展的结果都会立刻受到密码学界的审视。此次发布也助长了这样一种更宏观的叙事：AI 辅助系统正在以很快的速度在纯数学领域产出新成果。 据 Hacker News 用户 gukoff 的分析，该整数分解结果建立在通用数域筛法（GNFS）之上，而 GNFS 的渐近复杂度本就远优于这一新算法。Cogentic 并未证明 GNFS 所依赖的三个未经证明的启发式假设，而是替换了 GNFS 中依赖这些假设的部分，并为此付出了相当大的复杂度代价，因此这并非对现网密码系统的实际攻破。

hackernews · rgwohlbold · 11月25日 13:33 · [社区讨论](https://news.ycombinator.com/item?id=50642086)

**背景**: 整数分解是指把一个合数写成若干素数之积的问题；许多公钥密码方案（最著名的是 RSA）都建立在大整数难以分解这一假设之上。离散对数问题——即在某个群中给定 g^x = h 求出指数 x——则是支撑 Diffie-Hellman 密钥交换和 ElGamal 加密的同类困难问题。通用数域筛法是已知最优秀的经典大整数分解算法；而在足够大的量子计算机上运行 Shor 算法，这两个问题都能在多项式时间内求解。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Integer_factorization">Integer factorization - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Discrete_logarithm">Discrete logarithm - Wikipedia</a></li>
<li><a href="https://news.ycombinator.com/item?id=50642086">Google releases Cogentic papers on integer factorization , discrete ...</a></li>

</ul>
</details>

**社区讨论**: 讨论中的情绪在兴奋与怀疑之间摇摆：有评论者把这一结果视为 AI 驱动数学发现浪潮的一部分（其中一位将其类比为 AlphaGo 对围棋搜索空间的探索），也有人感叹在 AI 市场下滑之际却不断出现惊人的研究进展。最具实质性的质疑来自 gukoff，他认为该分解进展在渐近意义上不如 GNFS，并指出人们对 AI 生成证明的接受门槛已大幅提高；另有评论者援引可信人士的传闻称，这只是“更大成果的冰山一角”。

**标签**: `#cryptography`, `#integer-factorization`, `#number-theory`, `#google-research`, `#ai-for-math`

---

<a id="item-5"></a>
## [开发者用 Lean 审计 Clojure 核心库，发现未报告缺陷](https://s.conao3.com/blog/2026/e4f733) ⭐️ 8.0/10

一位开发者使用 Lean 证明助手分析 Clojure 的核心库（clojure.core），并公布了一份此前未被报告的缺陷清单，相关博文登上 Hacker News 首页，获得 211 分和 73 条评论。这项工作的特别之处在于，它把一个依赖类型论的证明助手用于审计一门动态类型、运行在 JVM 上的语言的核心库，而不是用来验证某个专门编写的算法。 Clojure 核心库支撑着庞大的生产生态——收购了 Rich Hickey 旗下 Cognitect 的 Nubank 就在其上运行大量关键基础设施——因此在 `get` 这类基础函数和 Java 互操作调用中发现潜在边界缺陷，对众多下游用户意义重大。更广泛地看，这一实验显示证明助手类工具正从纯数学和形式化证明领域延伸到实际的代码审计，同时也引出关于噪声、误报以及如何甄别这类报告的问题。 评论者对其中至少两项发现提出反驳，认为它们是由类型不匹配导致的误报，普通的类型检查就能发现：`(.indexOf (seq (byte-array [1 2 3])) 2)` 会失败，因为参数是 Long 而字节数组存放的是 byte；`(get "abc" 1.9)` 会失败，是因为在字符串场景下 `get` 会把键强制转换为整数。这说明该审计的价值在很大程度上取决于能否过滤噪声，而部分被报告的“缺陷”其实是 Java 互操作被误用或是有意为之的强制转换语义，而非 Clojure 本身的缺陷。

hackernews · encyclopedism · 11月25日 14:56 · [社区讨论](https://news.ycombinator.com/item?id=50642939)

**背景**: Lean 是一门开源编程语言兼证明助手，旨在编写正确、可维护且经过形式化验证的代码；2021 年研究团队用它形式化了 Peter Scholze 在凝聚态数学领域的一个证明，使其广受关注。Clojure 是运行在 JVM 上的 Lisp 方言，其 `clojure.core` 命名空间提供了语言的大部分标准函数，而由于 Clojure 是动态类型语言，许多类型错误只有在运行时才会暴露。形式化验证与普通的静态分析不同：静态分析器从源码中推导控制流与数据流信息，而证明助手允许你陈述某个性质，并由机器检查该性质对所有输入都成立的证明——因此要把 Lean 应用于一门现有动态语言的库，需要对该库的语义进行建模。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://lean-lang.org/">Lean Programming Language</a></li>
<li><a href="https://clojuredocs.org/clojure.core">clojure.core namespace | ClojureDocs - Community-Powered ...</a></li>

</ul>
</details>

**社区讨论**: 总体情绪是认可这项工作的努力，但对其精确性提出批评：一位评论者指出两项误报，认为这类审计若能减少噪声会有用得多；另一位则提到自己做过类似的审计，在 SBCL、Clozure CL 和 ACL2 中发现了数十个问题。也有人指出，像 Nubank 这样的重量级 Clojure 用户本应让人以为核心基础函数是毫无瑕疵的；还有评论者追问，Lean 如今是否已取代 Rocq（原 Coq）用于程序验证，以及语言模型是否只是更擅长写 Lean 而已。

**标签**: `#Clojure`, `#Lean`, `#formal-verification`, `#static-analysis`, `#programming-languages`

---

<a id="item-6"></a>
## [美国出台新规，堵住远程调用先进 AI 芯片的漏洞](https://t.me/zaihuapd/45361) ⭐️ 8.0/10

美国商务部工业与安全局（BIS）在 11 月中旬发布临时最终规则，把对先进 AI 芯片和服务器的出口管制从实体出口延伸到“远程访问”，以防止企业借第三国数据中心绕过算力限制。新规还要求向印度尼西亚、马来西亚、新加坡、泰国和巴西再出口 AI 芯片时必须申请许可，据报道该规则由财政部和国家安全委员会主导起草。 这堵上了监管机构眼中芯片管制体系里最大的一个缺口：此前中国企业可以在第三国的数据中心里，用美国设计的加速器训练前沿模型，而受管制的物项本身从未跨越受控边境。新规将直接影响云服务商、数据中心运营商和芯片出口商，并进一步收窄中国获取先进 AI 算力的渠道。 规则要求数据中心、海外晶圆代工厂和芯片出口商对客户进行严格的尽职调查，包括核查客户是否被 D:5 组国家或澳门的主体直接或间接拥有、控制，同时该规则还伴随着此前“AI 扩散规则”（AI Diffusion Rule）的撤销。由于是“临时最终规则”，它在征求意见的同时基本立即生效。

telegram · zaihuapd · 11月25日 11:35

**背景**: 根据美国《出口管理条例》（EAR），“再出口”（reexport）指受管制物项从一个外国运往或传输到另一个外国，区别于从美国本土的“出口”；传统上管制针对的是实体物项以及特定技术和软件。先进 AI 加速器已成为训练大模型的核心瓶颈，因此美国政策不断加码，试图限制谁能买到这些芯片、它们能被部署在哪里。此前的“AI 扩散规则”试图按国家分级管理 AI 芯片的全球分销，但遭到产业界和盟友的强烈批评，如今被这套更聚焦远程访问与云端访问的思路所取代。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.federalregister.gov/documents/2026/11/19/2026-23529/addressing-remote-access-to-advanced-semiconductors">Addressing Remote Access to Advanced ... - Federal Register</a></li>
<li><a href="https://www.gtlaw.com/en/insights/2026/11/bis-interim-final-rule-targets-remote-access-to-advanced-semiconductors-rescinds-ai-diffusion-rule">BIS Interim Final Rule Targets Remote Access to Advanced ...</a></li>
<li><a href="https://www.orrick.com/en/Insights/2026/11/US-Government-Establishes-Export-Controls-to-Address-China-AI-Remote-Access-Concerns">U.S. Government Establishes Export Controls to Address China ...</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#export controls`, `#US policy`, `#semiconductors`, `#cloud computing`

---

<a id="item-7"></a>
## [Minecraft Java 版 1.20.5 起全版本受高危 RCE 漏洞影响，恶意字体可远程执行代码](https://github.com/bikini/minecraft2shell) ⭐️ 8.0/10

11 月 22 日公开的 minecraft2shell 概念验证显示，服务器资源包中特制的 TrueType 字体可触发 FreeType 2.14.3 及更早版本的原生越界写，从而在 Windows 客户端上对 Minecraft Java 版 1.20.5 至 1.21.10 以及 26.1 至 26.4 快照执行任意代码。Mojang 尚未发布官方补丁，仍内置 lwjgl-freetype 3.4.3，社区已于 11 月 24 日推出名为 m2sfix 1.0.0 的临时缓解方案，以 Java agent 或 mod 形式关闭字体 hinting。 由于资源包可由服务器自动下发，玩家仅仅加入一个恶意或被攻陷的多人服务器就可能被植入代码，这让一个日常操作变成了影响数亿玩家的远程代码执行入口。Mojang 迟迟未发布官方补丁，使 Windows 平台的 Java 版用户只能依赖第三方 mod 或手动禁用服务器资源包，也让人质疑游戏对可下载客户端资源的信任边界是否过大。 该漏洞本质是 FreeType 在 TrueType hinting 处理路径上的原生内存破坏，因此它并非纯粹的 Java 沙箱逃逸，而是在 JVM 内存安全保护之外执行代码；据报告 1.20.4 及更早版本和基岩版不受影响，影响范围限于 Windows 客户端。在修复发布前，投稿人建议不要添加任何资源包、将多人游戏服务器资源包权限设为“禁用”，或安装 m2sfix 1.0.0 代理/mod。

telegram · zaihuapd · 11月25日 12:46

**背景**: FreeType 是广泛使用的开源字体光栅化库，其 TrueType hinting 代码会执行字体文件中内嵌的指令，以便将字形对齐到像素网格，这是一个能力强大但历史上屡出漏洞的攻击面。Minecraft Java 版正是通过 LWJGL 的 lwjgl-freetype 绑定来渲染文字，因此资源包内的字体文件会由游戏进程中的这段原生代码解析。此类越界写漏洞（例如 FreeType 的 CVE-2025-27363）可以让攻击者破坏内存并劫持执行流，这就是一个字体文件能变成 RCE 原语的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nhimg.org/glossary/cve-2025-27363-freetype-out-of-bounds-write/">What Is CVE-2025-27363 (FreeType Out-of-Bounds Write)?</a></li>
<li><a href="https://freetype.org/freetype2/docs/hinting/hinting.html">FreeType Hinting</a></li>
<li><a href="https://javadoc.lwjgl.org/org/lwjgl/util/freetype/FreeType.html">FreeType ( LWJGL 3.4.2-snapshot)</a></li>

</ul>
</details>

**标签**: `#Minecraft`, `#RCE`, `#FreeType`, `#Security Vulnerability`, `#Java`

---

<a id="item-8"></a>
## [三星电子与 SK 海力士据称将通过交叉许可采用长江存储 Xtacking 技术](https://t.me/zaihuapd/45377) ⭐️ 8.0/10

据报道，三星电子和 SK 海力士已通过交叉许可协议，同意在 3D NAND 闪存中采用长江存储（YMTC）Xtacking 堆叠技术的部分内容。三方均对此拒绝置评，该消息目前尚未得到官方确认。 若消息得到证实，这将意味着存储技术知识产权的流动方向出现明显反转——韩国巨头反而向中国挑战者授权工艺架构。随着 3D NAND 垂直微缩愈发困难，这也可能推动晶圆键合架构在整个行业加速普及。 Xtacking 的做法是将存储单元阵列与 CMOS 逻辑控制电路分别制作在两片晶圆上，再通过键合工艺合二为一，使两部分可以各自独立生产与优化。Omdia 分析师指出，这样 NAND 厂商可以自行生产存储阵列，而把逻辑电路交给晶圆代工厂，从而用上更先进的制程。

telegram · zaihuapd · 11月26日 05:30

**背景**: 3D NAND 将存储单元在垂直方向上堆叠，业界传统上要么把 CMOS 控制电路放在阵列旁边（传统并列式架构），要么放在阵列下方（CuA，即 CMOS under Array 架构）。长江存储的 Xtacking 架构始于 2018 年，目前已发展到 3.0 版本，其做法是把单独制造的 CMOS 晶圆与阵列晶圆键合在一起，公司称这可带来更高速的接口和更大的灵活性。交叉许可是指两个或多个专利权人相互授予对方技术使用权的安排，通常用于避免侵权诉讼、降低交易成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ymtc.com/cn/technicalintroduction.html">晶栈® Xtacking ®先进架构- 长 江 存 储</a></li>
<li><a href="https://developer.aliyun.com/article/1100149">长 江 存 储 YMTC Xtacking 技 术 演进与芯片级解密-开发者社区-阿里云</a></li>
<li><a href="https://wiki.mbalib.com/wiki/交叉许可">交叉许可 - MBA智库百科</a></li>

</ul>
</details>

**标签**: `#3D NAND`, `#semiconductor manufacturing`, `#Xtacking`, `#cross-licensing`, `#memory technology`

---