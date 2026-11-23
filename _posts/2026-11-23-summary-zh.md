---
layout: default
title: "Horizon Summary: 2026-11-23 (ZH)"
date: 2026-11-23
lang: zh
---

> 从 25 条内容中筛选出 3 条重要资讯。

---

1. [OpenAI 论证更低困惑度与更强模型智能相关](#item-1) ⭐️ 8.0/10
2. [Masullo 争议性证明的 Lean 形式化进度图引发审视](#item-2) ⭐️ 8.0/10
3. [Z.ai 发布 GLM-5.3-Flash：18B 激活多模态模型，价格仅上代十分之一](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 论证更低困惑度与更强模型智能相关](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 8.0/10

OpenAI 发布了由首席科学家 Jakub Pachocki 撰写的分析文章，认为更低的困惑度——即模型预测和压缩原始数据的能力——与更强的模型智能高度相关。文章展示了一张从 GPT-3.5 开始追踪 OpenAI 模型该指标变化的图表，并称这一单一指标能够描述出乎意料广泛的能力范围。 这一主张的重要性在于，困惑度是一种简单且成本较低的预训练指标；如果它能可靠反映模型能力，就可能比日益复杂的一整套评测提供更清晰的基准。随着模型越来越多地依赖强化学习，这也引发了关于下一词预测和压缩能在多大程度上体现推理能力的疑问。 讨论指出，文章并未正式定义困惑度，而且图表中的指标是预训练下一词预测模型在测试集上的困惑度，并非下游任务表现的直接度量。困惑度还取决于分词器、词表大小和评测数据集，因此跨模型比较需要共同的留出基准才有意义。

hackernews · acossta · 11月22日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50601525)

**背景**: 在信息论中，困惑度衡量概率模型在预测序列中每个下一词时的“惊讶”程度；完美预测器的困惑度为 1，而在大小为 N 的词表上随机预测的困惑度为 N。困惑度越低，说明模型给真实数据分配的概率越高，这在数学上等价于对数据更好的压缩。压缩与智能相关联的观点由来已久，评论者将 OpenAI 的论证与更早的工作联系起来，那些工作认为对原始数据的预测率体现了模型构建复杂世界模型的进展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>
<li><a href="https://news.ycombinator.com/item?id=50601525">Perplexity and Intelligence | Hacker News</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论非常热烈，评论者对在转向强化学习训练后交叉熵损失仍能反映模型能力表示惊讶，并欢迎在评测日益复杂之际出现一个简单基准。也有人批评文章没有定义困惑度，将这一论点与 2008 年一篇关于压缩与智能的论文联系起来，并分享了一条 X 帖子，称微软的 Mustafa Suleyman 在 OpenAI 的评测集上报告 MAI-2 Base 的对数困惑度为 0.819。

**标签**: `#perplexity`, `#language-models`, `#evaluation-metrics`, `#compression`, `#AI-research`

---

<a id="item-2"></a>
## [Masullo 争议性证明的 Lean 形式化进度图引发审视](https://claude.ai/artifact/CtQyX8qfYAF822bgHJHHE3) ⭐️ 8.0/10

一份追踪 Alessandro Masullo 手稿 Lean 形式化进度的公开进度图以 Claude artifact 的形式发布，并在 Hacker News 上引发热议（196 个赞、154 条评论）。该进度图对应一个开放的 GitHub 仓库，志愿参与的数学家正在把这份手稿的论证翻译成 Lean 代码，页面则可视化了目前已经完成的工作量。 这一事件说明，形式化的进度很容易被误读为“证明正确”的证据，而数学界真正用来甄别非凡断言的手段，是勘误清单、专家评论以及公开表态保持距离，而非一份已完成的验证。对关注 AI 辅助工具、证明助手，以及数学界接受或否决重大结果之社会机制的读者而言，这件事都值得注意。 参与该项目的数学家 kopje_koffie 提醒说，勘误清单中的数百个问题有轻有重，目前还远不能判断核心思路是否存在致命漏洞；其他评论者则指出，只要有一个缺口，整个形式化工作就可能全盘崩塌。评论者还提到，最初代 Masullo 发布这一声称的 Ravi Vakil 现在表示自己根本没有看过该文档，而 Brian Conrad 对《科学美国人》表示这份手稿需要“大幅修改”。

hackernews · Qision · 11月22日 23:12 · [社区讨论](https://news.ycombinator.com/item?id=50605045)

**背景**: Lean 是一个开源证明助手兼函数式编程语言，基于带归纳类型的构造演算，自 2013 年起开发，目前由 Lean Focused Research Organization 支持，并拥有名为 mathlib 的大型社区数学库。所谓“形式化证明”，就是把定义和每一步推理都编码成代码，由 Lean 内核逐一机械校验，一旦整套论证能够编译通过，就能获得极高的可信度。但关键在于，一份只完成了一部分的形式化成果——例如一条进度条——并不能说明剩余缺口是否真的可以被补上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_theorem_prover">Lean theorem prover</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proof_formalization">Proof formalization</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proof_assistant">Proof assistant - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 整体情绪偏向怀疑：评论者反复警告不要把进度条当成“证明大体正确”的证据，有人判断该证明很可能存在重大漏洞，并认为其所用机制相比其他竞争性路线缺乏真正的突破感。一位项目贡献者则反驳了过度解读勘误清单的做法；另有评论者对万亿美元级公司的 AI 工具可能抢先完成数学家毕生投入的工作表达了更广泛的不安，认为这会让这一领域变得不再那么有趣。

**标签**: `#Lean`, `#formal verification`, `#mathematics`, `#proof formalization`, `#controversy`

---

<a id="item-3"></a>
## [Z.ai 发布 GLM-5.3-Flash：18B 激活多模态模型，价格仅上代十分之一](https://t.me/zaihuapd/45309) ⭐️ 8.0/10

Z.ai 发布了 GLM-5 系列首款原生多模态模型 GLM-5.3-Flash，总参数 320B、激活参数仅 18B。官方称其在多项编程和智能体基准上超过 GLM-5.2，API 价格约为上一代的十分之一，限时输入价格低至每百万 Tokens 0.075 美元。 这款模型以远低于上一代的 API 成本，将接近 Claude Opus 4.8 的编程与智能体能力带入市场，可能对高频调用的大规模开发者工作负载很有吸引力。它也会加剧中国大模型厂商之间的价格竞争，并对竞争对手的 API 定价形成压力。 限时优惠期间，API 输入价格为每百万 Tokens 0.075 美元，缓存输入为 0.015 美元，输出为 0.25 美元，缓存存储暂时免费；原文未披露标准原价。基准对比来自厂商自述，且优惠价格是临时性的。

telegram · zaihuapd · 11月23日 04:47

**背景**: 混合专家（MoE）模型包含多个专门的子网络，并由路由器为每个 token 只激活其中一部分，因此总参数 320B 的模型每次推理只使用 18B 激活参数，从而降低计算成本。原生多模态大模型从训练阶段就面向文本、图像等多种数据类型，而不是在事后外挂视觉能力。大模型 API 通常分别对输入、缓存输入和输出 Tokens 计费；提示缓存可在重复使用上下文时降低成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/multimodal-llm">What is a multimodal LLM (MLLM)? - IBM</a></li>
<li><a href="https://costperprompt.com/guides/how-llm-api-pricing-works">How LLM API Pricing Actually Works: Tokens, Caching, and ...</a></li>
<li><a href="https://developers.openai.com/api/docs/guides/prompt-caching">Prompt caching | OpenAI API</a></li>

</ul>
</details>

**标签**: `#LLM release`, `#multimodal`, `#MoE`, `#API pricing`, `#benchmarks`

---