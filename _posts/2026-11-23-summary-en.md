---
layout: default
title: "Horizon Summary: 2026-11-23 (EN)"
date: 2026-11-23
lang: en
---

> From 25 items, 3 important content pieces were selected

---

1. [OpenAI Links Lower Perplexity to Greater Model Intelligence](#item-1) ⭐️ 8.0/10
2. [Lean Formalization Progress Map for Masullo's Contested Proof Draws Scrutiny](#item-2) ⭐️ 8.0/10
3. [Z.ai releases GLM-5.3-Flash: 320B/18B-active multimodal model at one-tenth the price](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Links Lower Perplexity to Greater Model Intelligence](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 8.0/10

OpenAI published an analysis by Chief Scientist Jakub Pachocki arguing that lower perplexity—a measure of how well a model predicts and compresses raw data—correlates strongly with greater model intelligence. The post includes a plot tracking this metric across OpenAI models starting from GPT-3.5 and claims a surprisingly wide range of capabilities can be described by this single measure. The claim matters because perplexity is a simple, cheap pretraining metric, and if it reliably tracks capability it could offer a cleaner benchmark than the growing set of complicated evaluations. It also raises questions about how well next-token prediction and compression capture reasoning ability as models increasingly rely on reinforcement learning. The discussion notes that the article does not formally define perplexity, and that the metric shown is test-set perplexity for the pretrained next-token predictor rather than a direct measure of downstream task performance. Perplexity also depends on tokenizer, vocabulary, and evaluation set, so cross-model comparisons require a common held-out benchmark to be meaningful.

hackernews · acossta · Nov 22, 17:06 · [Discussion](https://news.ycombinator.com/item?id=50601525)

**Background**: In information theory, perplexity measures how surprised a probabilistic model is when predicting each next token in a sequence; a perfect predictor has perplexity 1, while a random predictor over a vocabulary of size N has perplexity N. Lower perplexity means the model assigns higher probability to the actual data, which is mathematically equivalent to better compression of that data. The idea that compression and intelligence are linked has a long history, and commenters connected OpenAI's argument to earlier work arguing that prediction rate on raw data captures progress toward sophisticated world models.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>
<li><a href="https://news.ycombinator.com/item?id=50601525">Perplexity and Intelligence | Hacker News</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread was highly engaged, with commenters expressing surprise that cross-entropy loss still tracks capability despite the shift toward RL-based training and welcoming a simple benchmark amid increasingly convoluted evaluations. Others criticized the article for not defining perplexity, connected the thesis to a 2008 paper on compression and intelligence, and shared an X post in which Microsoft's Mustafa Suleyman reportedly reports MAI-2 Base log-perplexity of 0.819 on OpenAI's evaluation set.

**Tags**: `#perplexity`, `#language-models`, `#evaluation-metrics`, `#compression`, `#AI-research`

---

<a id="item-2"></a>
## [Lean Formalization Progress Map for Masullo's Contested Proof Draws Scrutiny](https://claude.ai/artifact/CtQyX8qfYAF822bgHJHHE3) ⭐️ 8.0/10

A public progress map tracking the Lean formalization of Alessandro Masullo's manuscript has been published as a Claude artifact and discussed heavily on Hacker News (196 upvotes, 154 comments). The map corresponds to an open GitHub repository where volunteer mathematicians are translating the manuscript's arguments into Lean, and the page visualizes how much of the work has been completed so far. The episode illustrates how formalization progress can be misread as evidence that a proof is correct, and how the mathematical community polices extraordinary claims through errata lists, expert commentary, and public distancing rather than through a finished verification. It matters to anyone following the intersection of AI-assisted tooling, proof assistants, and the social process by which mathematics accepts or rejects major results. A contributing mathematician (kopje_koffie) cautions that the hundreds of errata issues range from minor to significant and that it is still too early to tell whether there is a fatal hole in the core idea, while other commenters note that a single gap is enough to collapse an entire formalization effort. Commenters also report that Ravi Vakil, who originally announced the claim on Masullo's behalf, now says he has not even examined the document, and that Brian Conrad told Scientific American the manuscript needs "major revision".

hackernews · Qision · Nov 22, 23:12 · [Discussion](https://news.ycombinator.com/item?id=50605045)

**Background**: Lean is an open-source proof assistant and functional programming language based on the calculus of constructions with inductive types, developed since 2013 and now supported by the Lean Focused Research Organization, with a large community mathematics library known as mathlib. Formalizing a proof means encoding its definitions and every inference step so that the Lean kernel mechanically checks each one, which yields extremely high confidence once the whole argument compiles. Crucially, a partially finished formalization—such as a progress bar—says nothing about whether the remaining gaps can actually be closed.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_theorem_prover">Lean theorem prover</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proof_formalization">Proof formalization</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proof_assistant">Proof assistant - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The overall sentiment is skeptical: commenters repeatedly warn against reading the progress bar as evidence the proof is largely correct, and several describe the claim as likely containing a major hole and note the supporting machinery feels less novel than competing approaches. A contributor pushes back on over-interpreting the errata list, while one commenter expresses broader unease that a trillion-dollar company's AI tooling may finish formalizing work that mathematicians spent careers on, making the field feel less interesting.

**Tags**: `#Lean`, `#formal verification`, `#mathematics`, `#proof formalization`, `#controversy`

---

<a id="item-3"></a>
## [Z.ai releases GLM-5.3-Flash: 320B/18B-active multimodal model at one-tenth the price](https://t.me/zaihuapd/45309) ⭐️ 8.0/10

Z.ai has launched GLM-5.3-Flash, the first native multimodal model in its GLM-5 series, with 320B total parameters and only 18B active parameters. The company says it beats GLM-5.2 on multiple coding and agent benchmarks and comes at roughly one-tenth the previous generation's API price, with limited-time input pricing as low as $0.075 per million tokens. The release puts a highly efficient mixture-of-experts model with coding and agent capabilities near Claude Opus 4.8 into the market at a fraction of prior API costs, which could make it attractive for high-volume developer workloads. It also intensifies price competition among Chinese LLM providers and raises pressure on rivals' API pricing. During the limited-time promotion, API pricing is $0.075 per million input tokens, $0.015 per million cached input tokens, and $0.25 per million output tokens, with cache storage temporarily free; the standard prices were not disclosed in the item. The benchmark comparisons are vendor-reported, and the promotional rates are temporary.

telegram · zaihuapd · Nov 23, 04:47

**Background**: Mixture-of-experts (MoE) models contain many specialized sub-networks and a router that activates only a subset for each token, so a 320B-total model can use just 18B active parameters per pass and cut compute costs. A native multimodal LLM is trained to handle multiple data types such as text and images rather than adding vision capabilities after the fact. LLM APIs typically bill separately for input, cached input, and output tokens; prompt caching lowers costs when repeated context is reused.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/multimodal-llm">What is a multimodal LLM (MLLM)? - IBM</a></li>
<li><a href="https://costperprompt.com/guides/how-llm-api-pricing-works">How LLM API Pricing Actually Works: Tokens, Caching, and ...</a></li>
<li><a href="https://developers.openai.com/api/docs/guides/prompt-caching">Prompt caching | OpenAI API</a></li>

</ul>
</details>

**Tags**: `#LLM release`, `#multimodal`, `#MoE`, `#API pricing`, `#benchmarks`

---