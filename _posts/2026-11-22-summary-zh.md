---
layout: default
title: "Horizon Summary: 2026-11-22 (ZH)"
date: 2026-11-22
lang: zh
---

> 从 23 条内容中筛选出 5 条重要资讯。

---

1. [Lean 形式化验证黎曼猜想引发信任与 AI 争论](#item-1) ⭐️ 9.0/10
2. [GPGME 远程代码执行漏洞影响 2.3.0 之前的所有版本](#item-2) ⭐️ 8.0/10
3. [微软将 RDMA over USB4 引入 Windows，多台 PC 可合跑一个本地 AI 模型](#item-3) ⭐️ 8.0/10
4. [浙江大学在超导芯片上首次真机实现 QRAM](#item-4) ⭐️ 8.0/10
5. [美商务部将定稿新规，封堵中国 AI 公司远程使用先进芯片](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Lean 形式化验证黎曼猜想引发信任与 AI 争论](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 9.0/10

Lean 社区博客发布了对黎曼猜想的形式化验证，并据称同时确认了广义黎曼猜想；Anthropic 数学家 Levent Alpöge 表示 Claude 协助形式化了大量现代数学内容，详细证明文稿超过 25 万页。 如果该验证成立，这将是数学与形式化方法领域的范式转变，表明 AI 辅助形式化能够攻克基础性难题，并可能重塑证明的检查与信任方式。 该结论依赖 Lean 内核及独立检查器；评论者指出此前一个伪造的 Collatz 反证曾利用 Lean 内核漏洞，但如今存在多个独立实现及一致性证明，使同时影响 GRH 证明和所有内核的漏洞概率极低。证明以 Lean 代码而非传统论文形式呈现，25 万页文稿与 Claude 的参与使独立检查和专家复核尤为关键。

hackernews · g-b-r · 11月21日 14:36 · [社区讨论](https://news.ycombinator.com/item?id=50589618)

**背景**: Lean 是一个开源证明助手和函数式编程语言，基于依赖类型论，可把数学定义、命题和证明编码为机器可检查的形式。形式化验证意味着证明由一个小型可信内核而非仅靠人工审阅来检查。黎曼猜想由 Bernhard Riemann 于 1859 年提出，涉及素数分布规律，是数学中最著名的未解难题之一；其推广形式广义黎曼猜想（GRH）将猜想扩展到更广泛的一类 L 函数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_theorem_prover">Lean theorem prover</a></li>
<li><a href="https://lawrencecpaulson.github.io/2026/07/30/Collatz.html">Why is it all in the kernel ?</a></li>

</ul>
</details>

**社区讨论**: 评论者总体印象深刻但态度谨慎：有人认为多个独立内核和一致性证明使“内核漏洞导致错误”的可能性微乎其微，也有人提起此前的伪造 Collatz 反证，强调检查器并非完全独立。多人把功劳归于 Levent Alpöge 的专家指导，并认为 Claude 辅助形式化大量现代数学内容本身就是一项重大成果。

**标签**: `#formal-verification`, `#lean`, `#riemann-hypothesis`, `#mathematics`, `#ai-assisted-proofs`

---

<a id="item-2"></a>
## [GPGME 远程代码执行漏洞影响 2.3.0 之前的所有版本](https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) ⭐️ 8.0/10

GPGME（GnuPG 的 C 语言库接口）中的一个远程代码执行漏洞于 2026 年 11 月 20 日公开披露，影响 2.3.0 之前的所有版本。该漏洞由 Johan Carlsson 发现，GitLab 于 2026 年 11 月 12 日通知 GPGME 维护者；由于 GitLab 需要随 Ruby2Shell 更新提前发布修复，协同披露日期从原定的 2026 年 11 月 25 日提前到 11 月 20 日。 GPGME 以动态库、DLL 或静态链接的方式被大量软件使用，包括 Gpg4win、GnuPG Desktop、大多数邮件客户端、许多 XMPP 客户端、Samba 和 Flatpak，因此一个漏洞会波及非常广泛的下游生态。GitLab 对签名提交的支持使得该路径上的代码执行尤为危险，下游打包者现在必须排查自己分发的库副本是否受影响。 评论者指出，底层缺陷实际上是一个双重释放（double free），而非完整的 RCE 利用链，因此“远程代码执行”的标签可能夸大了实际可利用性。值得注意的是，Red Hat 似乎早在约五年前就依据常规静态分析工具的输出在下游修复了该缺陷，而上游 GPGME 却一直未能发现。

hackernews · gdgghhhhh · 11月21日 08:32 · [社区讨论](https://news.ycombinator.com/item?id=50587208)

**背景**: GPGME 全称 “GnuPG Made Easy”，是一个 C 语言库，为应用程序提供稳定的编程接口，以便调用 GnuPG 或 GpgSM 等引擎完成加密操作，从而不必直接调用 gpg 可执行文件。由于它用 C 编写，双重释放、缓冲区溢出等缺陷属于内存安全问题：它们会破坏内存，最坏情况下可被利用实现任意代码执行。协同漏洞披露是指报告者私下通知维护者，并在约定时间同时发布修复与公开公告的流程，这也正是此次 GitLab 提前披露日期之所以重要的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/gpg/gpgme">GitHub - gpg/gpgme: GnuPG Made Easy. NOTE: Maintainers are ...</a></li>
<li><a href="https://www.gnupg.org/documentation/manuals/gpgme/">Top (The ‘GnuPG Made Easy’ Reference Manual)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Memory_safety">Memory safety - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者对报道的定性提出质疑，有人直言“这是双重释放漏洞，不是 RCE 利用链”，并追问此类漏洞报告是否有意夸大。其他人则梳理了受影响的下游范围——Samba、邮件与 XMPP 客户端、Flatpak、Gpg4win——并询问 apt 等工具是否受影响；还有人借此争论，认为人类不应在没有 Rust 级别工具保障的情况下编写 C/C++ 代码。

**标签**: `#security`, `#vulnerability`, `#gnupg`, `#memory-safety`, `#open-source`

---

<a id="item-3"></a>
## [微软将 RDMA over USB4 引入 Windows，多台 PC 可合跑一个本地 AI 模型](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 8.0/10

微软发布了 Windows 上 RDMA over USB4 的开发者预览版，多台 PC 可通过普通 USB4 线缆共享内存与 GPU 算力，共同运行同一个本地 AI 大模型，无需专用网卡或交换机。演示中三台搭载 AMD Ryzen AI Max+ 395 的系统以 4-bit 量化运行 Qwen3-235B-A22B，速度约为 18.5 token/s，该功能将通过 Windows Insider 渠道推送。 这让几台普通的 Windows 电脑借助用户已有的接口和线缆组成一个小型推理集群，使发烧友和小团队能够运行远超单台消费级 PC 内存容量的模型。这也表明微软正在把分布式本地 AI 基础设施直接做进 Windows，为不想租用云 GPU 或购买工作站级硬件的用户提供了另一条路径。 该能力目前只是开发者预览而非正式功能，因此会先推送给 Windows Insider 测试者，应视为实验性特性。有报道称，相比同样走 USB4 的以太网方案，这一 USB4 直连路径的延迟明显更低，但聚合内存与互联带宽仍远不及数据中心级网络，且约 18.5 token/s 的成绩是在激进使用 4-bit 量化的前提下取得的。

telegram · zaihuapd · 11月21日 06:13

**背景**: RDMA（远程直接内存访问）允许一台机器直接读写另一台机器的内存，绕过普通网络带来的大量 CPU 与操作系统开销，长期以来是 InfiniBand、RoCE 等数据中心网络的核心技术。USB4 可以隧道传输 PCIe，并用廉价且普及的线缆提供高带宽，因此成为在消费级 PC 之间承载 RDMA 的可行选择。演示所用的 Qwen3-235B-A22B 是阿里巴巴通义千问团队的混合专家（MoE）模型，总参数 2350 亿，但每个 token 仅激活约 220 亿参数，因此它需要极大的总内存、但计算需求相对温和。把权重压缩到 4-bit 可将内存占用相比 16-bit 降低约 75%，这正是让模型能拆分到多台机器上运行的关键。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcommunity.microsoft.com/blog/microsoftusbblog/introducing-rdma-over-usb4®-on-windows-run-larger-local-ai-models-across-pcs/4574602">Introducing RDMA over USB4® on Windows: run larger local AI ...</a></li>
<li><a href="https://windowsreport.com/windows-pcs-can-now-team-up-over-usb4-to-run-ai-models-that-wont-fit-on-one-machine/">Windows PCs Can Now Team Up Over USB4 to Run AI Models That ...</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3-235B-A22B">Qwen/Qwen3-235B-A22B · Hugging Face</a></li>

</ul>
</details>

**标签**: `#Microsoft`, `#USB4`, `#RDMA`, `#local AI`, `#distributed inference`

---

<a id="item-4"></a>
## [浙江大学在超导芯片上首次真机实现 QRAM](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 8.0/10

浙江大学团队在自主研制的超导量子芯片“天目 2 号”上首次于真机实现量子随机存储器（QRAM），分别以 80.9% 和 60.4% 的准确率完成 4 位与 8 位数据调取，成果发表于《自然·物理》。 QRAM 是将经典数据加载到量子叠加态中的关键部件，被视为许多量子算法实现加速的前提，因此真机原型标志着其从理论方案迈向实验现实。但 8 位数据调取准确率明显下降，也说明可扩展、容错的 QRAM 仍是重大工程挑战。 该原型相较未优化方案将线路深度降低 30% 以上，并首次验证了局部抗噪特性；而从 4 位到 8 位调取准确率由 80.9% 降至 60.4%，则说明随着地址和数据位宽增加，误差会累积。团队表示下一步将推进 QRAM 的规模化研究。

telegram · zaihuapd · 11月21日 08:31

**背景**: 量子随机存储器（QRAM）利用量子比特以叠加态寻址存储单元，使量子计算机能够按需调取数据，为量子搜索、线性方程组求解等算法提供输入。该概念在 2008 年被形式化，提出用 O(log N) 个开关而非 N 个开关实现寻址，但物理实现一直很困难。超导量子比特是当前量子硬件的主流路线之一，“天目 2 号”即基于该技术，需要在极低温下运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC10490729/">Quantum Random Access Memory for Dummies - PMC</a></li>
<li><a href="https://link.aps.org/doi/10.1103/PhysRevLett.100.160501">Quantum Random Access Memory | Phys. Rev. Lett.</a></li>
<li><a href="https://baike.baidu.com/en/item/Tianmu-2/4929794">Tianmu-2_Baiduwiki - 百度百科</a></li>

</ul>
</details>

**标签**: `#quantum computing`, `#QRAM`, `#superconducting qubits`, `#hardware research`, `#Nature Physics`

---

<a id="item-5"></a>
## [美商务部将定稿新规，封堵中国 AI 公司远程使用先进芯片](https://t.me/zaihuapd/45289) ⭐️ 8.0/10

美国商务部正在敲定一项规则，禁止中国 AI 公司通过境外数据中心远程使用先进 AI 芯片，最早可能在本月公布。该规则将把现行半导体出口限制扩展至马来西亚、新加坡、泰国等七个国家，以封堵远程访问和芯片走私漏洞，目前正与其他政府机构磋商后定稿。 这填补了美国芯片出口管制中最大的剩余漏洞之一：中国企业此前可以不直接购买受限硬件，而是通过第三国租用算力。此举可能显著重塑中国大模型开发者可获取的全球 AI 算力格局，并直接波及英伟达——该公司一直主张限制海外部署会削弱美国 AI 基础设施的全球影响力。 据报道，该规则覆盖现有管制之外的七个国家，其中点名马来西亚、新加坡和泰国；白宫此前已要求国会立法，责成商务部制定这一规则。英伟达曾游说反对封堵这一远程访问缺口。消息源自 The Information，具体适用范围、算力门槛和生效日期尚未公开。

telegram · zaihuapd · 11月22日 04:34

**背景**: 自 2022 年以来，美国逐步限制向中国出口英伟达高端 GPU 等先进 AI 加速芯片，向中国买方销售需申请许可证。由于这些管制绑定的是硬件的实际出货，企业可以在不受管制的国家通过数据中心租用算力，从而部分绕开限制，即所谓“远程访问漏洞”。东南亚国家已成为此类算力的重要中转与托管枢纽，这也是新规重点针对这些国家的原因。

**标签**: `#AI chips`, `#export controls`, `#geopolitics`, `#semiconductors`, `#NVIDIA`

---