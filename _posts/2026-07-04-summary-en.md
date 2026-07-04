---
layout: default
title: "Horizon Summary: 2026-07-04 (EN)"
date: 2026-07-04
lang: en
---

> From 47 items, 10 important content pieces were selected

---

1. [Contrastive Decoding Diffing recovers finetuning data from logits alone](#item-1) ⭐️ 9.0/10
2. [EU Parliament Spyware Investigator Hacked by Pegasus](#item-2) ⭐️ 8.0/10
3. [Wordgard: New Rich-Text Editor from ProseMirror Creator](#item-3) ⭐️ 8.0/10
4. [Ubicloud Advocates Strict Memory Overcommit for PostgreSQL OOM Prevention](#item-4) ⭐️ 8.0/10
5. [AI Fears and LLMs Cause 50%+ Sales Drop in Developer Courses](#item-5) ⭐️ 8.0/10
6. [Anthropic Accuses Alibaba of Massive Distillation Attack on Claude](#item-6) ⭐️ 8.0/10
7. [Claude Fable 5 Relaunch Disappoints with Aggressive Safety Filters](#item-7) ⭐️ 8.0/10
8. [Huawei Launches Atlas 350 Card with Ascend 950PR, 2.87x H20 Performance](#item-8) ⭐️ 8.0/10
9. [NASA Launches Rescue Satellite to Boost Falling Swift Telescope](#item-9) ⭐️ 8.0/10
10. [Tencent Atuin AI beats Mythos in CyberGym at <0.1% cost](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Contrastive Decoding Diffing recovers finetuning data from logits alone](https://www.reddit.com/r/MachineLearning/comments/1umn2dk/contrastive_decoding_diffing_cdd_recovering/) ⭐️ 9.0/10

Contrastive Decoding Diffing (CDD) is a new grey-box method that recovers verbatim finetuning data from large language model logits without requiring weight access, activations, or a probe corpus. This breakthrough significantly advances model diffing for privacy and interpretability, exposing sensitive training data from fine-tuned models and revealing unexpected patterns like the recurring fictional persona 'Dr. Elena Rodriguez' across unrelated domains, which highlights risks from synthetic data generation. CDD uses a single default configuration without per-model calibration and achieves a verbatim recovery score of 4+/5 on 19 out of 20 model pairs across four model families (1B to 32B parameters) on the SDF benchmark, outperforming Activation Difference Lens (ADL), which requires full weight access and never exceeds 3/5.

reddit · r/MachineLearning · /u/CebulkaZapiekana · Jul 3, 19:01

**Background**: Model diffing is the study of mechanistic changes introduced during fine-tuning by comparing a fine-tuned model to its base model. Contrastive decoding is a text generation strategy that contrasts outputs from a strong model and a weak model to improve quality. CDD adapts this idea to model diffing by directly contrasting the logits of the base and fine-tuned models, whereas earlier methods like ADL required white-box access to activation differences.

<details><summary>References</summary>
<ul>
<li><a href="https://transformer-circuits.pub/2024/model-diffing/index.html">Stage-Wise Model Diffing</a></li>
<li><a href="https://github.com/science-of-finetuning/diffing-toolkit">science-of-finetuning/diffing-toolkit - GitHub</a></li>
<li><a href="https://www.geeksforgeeks.org/nlp/contrastive-decoding-in-natural-language-processing/">Contrastive Decoding in Natural Language... - GeeksforGeeks</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#model diffing`, `#LLM`, `#interpretability`, `#privacy`

---

<a id="item-2"></a>
## [EU Parliament Spyware Investigator Hacked by Pegasus](https://citizenlab.ca/research/member-of-committee-investigating-spyware-hacked-with-pegasus/) ⭐️ 8.0/10

Citizen Lab confirmed that a member of the European Parliament's committee investigating spyware was infected with Pegasus spyware in October 2022 and March 2023. This attack directly undermines the security of the European Parliament and raises serious concerns about state-sponsored surveillance targeting lawmakers investigating spyware abuses. The forensic analysis identified three distinct infection dates, with the first overlapping with a campaign targeting exiled journalists from Russia and Belarus in Europe.

hackernews · ledoge · Jul 3, 20:38 · [Discussion](https://news.ycombinator.com/item?id=48779683)

**Background**: Pegasus is a powerful spyware developed by Israeli firm NSO Group, capable of remotely infecting mobile devices through zero-click exploits. Citizen Lab is a renowned cybersecurity research group at the University of Toronto that has extensively documented Pegasus abuses.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Pegasus_(spyware)">Pegasus (spyware)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Citizen_Lab">Citizen Lab</a></li>

</ul>
</details>

**Discussion**: Comments highlight that Greece and other EU states have abused Pegasus, suggesting the attack may be domestic rather than foreign. Some question why the parliament allows personal and work data on the same device.

**Tags**: `#cybersecurity`, `#spyware`, `#European Parliament`, `#surveillance`, `#privacy`

---

<a id="item-3"></a>
## [Wordgard: New Rich-Text Editor from ProseMirror Creator](https://wordgard.net/) ⭐️ 8.0/10

Wordgard is a new in-browser rich-text editor announced by Marijn Haverbeke, the creator of ProseMirror, offering an improved architecture and features for building custom editors. It matters because it emerges from a highly respected developer in the rich-text editor ecosystem, potentially setting new standards or providing a more approachable alternative to ProseMirror's steep learning curve. Wordgard shares many concepts with ProseMirror but is not an upgrade path; switching requires significant work. The documentation includes a page comparing it to ProseMirror.

hackernews · indy · Jul 3, 08:50 · [Discussion](https://news.ycombinator.com/item?id=48772573)

**Background**: ProseMirror is a well-known open source library for creating customizable structured documents with a WYSIWYG interface. It has a modular architecture but a steep learning curve. Wordgard aims to address some of these limitations while maintaining similar concepts.

<details><summary>References</summary>
<ul>
<li><a href="https://prosemirror.net/">ProseMirror</a></li>
<li><a href="https://github.com/ProseMirror/prosemirror">ProseMirror/prosemirror: The ProseMirror WYSIWYM editor - GitHub</a></li>

</ul>
</details>

**Discussion**: Comments show a mix of interest and practical concerns. One commenter notes the lack of an upgrade path from ProseMirror, while another praises the design. A third discusses difficulties with static typing in ProseMirror, hinting at potential improvements in Wordgard.

**Tags**: `#rich-text-editor`, `#prosemirror`, `#web-development`, `#editor-framework`

---

<a id="item-4"></a>
## [Ubicloud Advocates Strict Memory Overcommit for PostgreSQL OOM Prevention](https://www.ubicloud.com/blog/postgresql-and-the-oom-killer-why-we-use-strict-memory-overcommit) ⭐️ 8.0/10

Ubicloud published a blog post explaining why they use strict memory overcommit (vm.overcommit_memory=2) for PostgreSQL to prevent the OOM killer from killing the database process. This matters because PostgreSQL's memory behavior makes it vulnerable to the OOM killer under default Linux overcommit settings, and strict overcommit can improve production database stability, though it requires careful tuning. The article describes three overcommit modes: heuristic (0), always (1), and strict (2). They recommend mode 2 for PostgreSQL, but caution that adjusting overcommit ratios without testing can prevent forks and crash applications.

hackernews · furkansahin · Jul 3, 13:00 · [Discussion](https://news.ycombinator.com/item?id=48774509)

**Background**: Linux kernel's overcommit memory policy controls whether the system allows memory allocation beyond physical RAM. When overcommit leads to memory exhaustion, the OOM killer terminates processes to free memory. PostgreSQL's memory management often allocates large amounts, making it a prime target for the OOM killer under default settings.

<details><summary>References</summary>
<ul>
<li><a href="https://linuxhandbook.com/oom-killer/">What is Out of Memory Killer (OOM Killer) in Linux?</a></li>
<li><a href="https://www.baeldung.com/linux/memory-overcommitment-oom-killer">Linux Memory Overcommitment and the OOM Killer - Baeldung Understanding and Utilizing the Linux OOM Killer - linuxvox.com memory - Understanding the Linux oom-killer's logs - Stack ... How to Configure the Linux Out-of-Memory Killer - Oracle Fix: Linux OOM Killer Killing Processes (Out of Memory)</a></li>
<li><a href="https://kernel-internals.org/mm/overcommit/">Memory Overcommit - Linux Kernel Internals</a></li>

</ul>
</details>

**Discussion**: Comments highlight mixed experiences: some praise strict overcommit for stability, while others warn about side effects like fork failures or system instability. Ubicloud's co-founder admits the title was too strong and acknowledges scenarios where strict overcommit may cause unanticipated issues.

**Tags**: `#PostgreSQL`, `#OOM killer`, `#memory management`, `#Linux`, `#production databases`

---

<a id="item-5"></a>
## [AI Fears and LLMs Cause 50%+ Sales Drop in Developer Courses](https://simonwillison.net/2026/Jul/3/josh-w-comeau/#atom-everything) ⭐️ 8.0/10

Course creator Josh W. Comeau reports that his new course 'Whimsical Animations' is on track to sell roughly one-third the copies of a typical launch, and his existing courses have seen sales down significantly from last year, with an overall decline of over 50%. This firsthand evidence highlights how AI fears and LLM-based tutoring are reshaping developer education, potentially threatening the business model of many online course creators and affecting how developers learn new skills. Comeau spoke to multiple course creators who all report the same trend: revenue down 50%+, fewer people engaging with content, and learners switching to LLMs that regurgitate creators' work without consent or compensation.

rss · Simon Willison · Jul 3, 21:25

**Background**: The rise of large language models (LLMs) like GPT-4 has enabled AI tools that can answer coding questions and provide tutoring, often for free or at low cost. This has led many developers to question the value of paid courses, especially amid fears that AI might replace developer jobs. Additionally, these models are trained on publicly available content, including online courses, without compensating the original creators.

**Tags**: `#AI`, `#developer education`, `#LLMs`, `#online courses`, `#industry trends`

---

<a id="item-6"></a>
## [Anthropic Accuses Alibaba of Massive Distillation Attack on Claude](https://t.me/zaihuapd/42327) ⭐️ 8.0/10

Anthropic sent a letter to the U.S. Senate Banking Committee accusing Alibaba of conducting a massive distillation attack on its Claude AI model, using nearly 25,000 fraudulent accounts to make over 28.8 million interactions between April 22 and June 5, 2026. In response, Alibaba reportedly ordered all employees to uninstall Claude-related products by July 10. This is the largest known distillation attack against a frontier AI model, highlighting escalating IP theft concerns between U.S. and Chinese AI companies. It underscores the vulnerability of publicly accessible AI APIs and could prompt stricter security measures and regulatory actions globally. Anthropic detected coordinated activity across a large number of accounts and deployed classifiers and behavioral fingerprinting to identify the attack. The accused parties include Alibaba and its AI lab Qwen, and the attack targeted Claude's capabilities, likely to replicate them in competing models.

telegram · zaihuapd · Jul 3, 06:21

**Background**: Distillation attacks (or model extraction attacks) involve repeatedly querying a proprietary AI model through its public API and using the input-output pairs to train a competing model, effectively stealing its capabilities. Such attacks have been flagged as a national security concern by the White House, especially in the context of US-China AI competition. Companies like Anthropic have built detection systems to identify these patterns and share indicators with other labs.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks">Detecting and preventing distillation attacks \ Anthropic</a></li>
<li><a href="https://www.cnbc.com/2026/06/24/anthropic-alibaba-distillation-campaign.html">Anthropic accuses Alibaba of campaign to extract AI capabilities What Are Distillation Attacks and How Can They Be Curbed AI distillation attacks in the US–China contest</a></li>
<li><a href="https://cloud.google.com/blog/topics/threat-intelligence/distillation-experimentation-integration-ai-adversarial-use">GTIG AI Threat Tracker: Distillation, Experimentation, and (Continued) Integration of AI for Adversarial Use | Google Cloud Blog</a></li>

</ul>
</details>

**Tags**: `#AI安全`, `#模型蒸馏`, `#Anthropic`, `#阿里巴巴`, `#知识产权`

---

<a id="item-7"></a>
## [Claude Fable 5 Relaunch Disappoints with Aggressive Safety Filters](https://www.bleepingcomputer.com/news/artificial-intelligence/claude-fable-relaunch-disappoints-users-with-nerfed-performance/) ⭐️ 8.0/10

Anthropic's Claude Fable 5 relaunched after export control lift, but users report that overly aggressive safety filters misclassify legitimate code, causing automatic downgrades to Opus 4.8 in many cases. This undermines developer trust and productivity, as the model's advanced capabilities are often unavailable during critical coding tasks, highlighting challenges in balancing safety and usability in AI deployment. The model's core performance remains unchanged, but the safety guardrails are set too high. Subscribers face usage quotas: only 50% weekly allocation until July 7, after which Fable 5 will require pay-per-use. API and enterprise pay-per-use versions retain full access.

telegram · zaihuapd · Jul 3, 07:20

**Background**: Claude Fable 5 is a publicly available version of Anthropic's Claude Mythos model, designed for advanced coding tasks. Anthropic initially withheld the model due to safety concerns about its ability to find software vulnerabilities. Upon relaunch, the company imposed stricter safety filters, leading to frequent false positives that degrade the developer experience.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Anthropic`, `#Claude`, `#Safety`, `#Developer Experience`

---

<a id="item-8"></a>
## [Huawei Launches Atlas 350 Card with Ascend 950PR, 2.87x H20 Performance](https://t.me/zaihuapd/42329) ⭐️ 8.0/10

At the 2026 Huawei China Partner Conference, Huawei officially launched and started selling the Atlas 350 AI training and inference accelerator card, featuring the new Ascend 950PR processor. The card claims 2.87 times the single-card compute of Nvidia's H20 and is the only accelerator in China supporting FP4 low-precision inference. This launch significantly challenges Nvidia's dominance in the AI hardware market, especially under US sanctions, by offering a domestically produced alternative with superior FP4 performance. It enables Chinese companies to run large models like 70B-parameter LLMs on a single card, reducing inference latency and deployment costs. The Atlas 350 features 112 GB of HBM memory and supports FP4 inference, which reduces memory footprint and speeds up calculations. Its vector compute power, interconnect bandwidth, and self-developed HBM have been substantially improved over the previous generation, enabling single-card loading of 70B-parameter models.

telegram · zaihuapd · Jul 3, 08:35

**Background**: FP4 (4-bit floating point) inference is a low-precision technique that represents model weights and activations in 4-bit format, reducing memory use and improving throughput while preserving accuracy. Huawei's Ascend series is a family of AI chips developed under U.S. export restrictions, with the 950PR being the latest high-end inference processor. The Nvidia H20 is a China-compliant GPU with reduced performance due to trade controls. Huawei's Atlas line of accelerators targets AI training and inference workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://tech-insider.org/huawei-ascend-950pr-ai-chip-nvidia-china-2026/">Huawei Ascend 950PR: The 1.56 PFLOP AI Chip vs Nvidia [2026]</a></li>
<li><a href="https://www.huaweicentral.com/ascend-950pr-ai-chip-everything-you-need-to-know/">Ascend 950PR AI Chip: Everything you need to know</a></li>
<li><a href="https://nerdleveltech.com/huawei-ascend-950pr-atlas-350-ai-chip-challenges-nvidia">Huawei Ascend 950PR Beats NVIDIA H20: 2.8× FP8, CUDA-Ready</a></li>

</ul>
</details>

**Tags**: `#AI Hardware`, `#Huawei`, `#Ascend 950PR`, `#Accelerators`, `#FP4`

---

<a id="item-9"></a>
## [NASA Launches Rescue Satellite to Boost Falling Swift Telescope](https://apnews.com/article/swift-nasa-satellite-rescue-katalyst-a7ddd740ca099587c58865f583c7245a) ⭐️ 8.0/10

On July 3, 2026, NASA launched the LINK spacecraft built by Katalyst Space, aiming to capture and boost the aging Swift gamma-ray burst observatory to a higher orbit, delaying its atmospheric reentry. This mission marks the first private spacecraft attempt to capture and service a U.S. government satellite, potentially revolutionizing satellite life extension and reducing space debris. It also ensures continued scientific observations of gamma-ray bursts. LINK will use a robotic arm to latch onto Swift and then boost its orbit by about 240 km. If successful, Swift could resume operations as early as September.

telegram · zaihuapd · Jul 3, 15:43

**Background**: Swift, launched in 2004, observes gamma-ray bursts (GRBs) and has been crucial for multi-wavelength astronomy. Due to atmospheric drag from solar activity, its orbit has been decaying, and without intervention it could burn up in the atmosphere by October. The LINK spacecraft is a commercial robotic servicer designed for satellite life extension.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nasa.gov/image-article/link-spacecraft-set-for-mission-to-boost-nasas-swift-observatory/">LINK Spacecraft Set for Mission to Boost NASA ’s Swift... - NASA</a></li>
<li><a href="https://www.cbsnews.com/news/nasa-mission-rescue-falling-swift-telescope/">Mission launched to save falling Swift space telescope - CBS News</a></li>
<li><a href="https://www.dw.com/en/swift-boost-mission-an-opportunity-for-science-and-defense/a-77768927">NASA 's Swift Boost mission : chance for science and defense</a></li>

</ul>
</details>

**Tags**: `#space`, `#NASA`, `#satellite servicing`, `#astronomy`

---

<a id="item-10"></a>
## [Tencent Atuin AI beats Mythos in CyberGym at <0.1% cost](https://mp.weixin.qq.com/s/BzU7g-2iG7d6h4ViwMhxyg) ⭐️ 8.0/10

Tencent Xuanwu Lab's Atuin AI, built on the open-source GLM-5.1 model, scored 84% on the UC Berkeley-led CyberGym benchmark, surpassing Anthropic's Claude Mythos Preview. It also discovered multiple high-risk logic vulnerabilities in projects like curl and OpenSSL that Mythos missed. This demonstrates that open-source AI models can outperform proprietary ones in specialized cybersecurity tasks at a fraction of the cost, potentially democratizing vulnerability discovery. It also shows that models deployed locally can identify real-world critical vulnerabilities, validated by Berkeley rankings. Atuin AI consumed less than 0.1% of the budget of Mythos's 'Glasswing Project'. In the Berkeley BVI real-world vulnerability list, Atuin ranked 1st in severity and 5th in total number of discovered vulnerabilities, with the highest CVSS score reaching 9.3.

telegram · zaihuapd · Jul 3, 16:12

**Background**: CyberGym is a large-scale benchmark created by UC Berkeley that evaluates AI agents on real-world vulnerability analysis tasks, featuring 1,507 vulnerabilities across 188 projects. GLM-5.1 is an open-weight large language model developed by Z.AI (formerly Zhipu AI), released under the MIT License. Claude Mythos is a proprietary model from Anthropic designed for cybersecurity, but it has not been publicly released due to safety concerns.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/sunblaze-ucb/cybergym">GitHub - sunblaze-ucb/cybergym: CyberGym is a large-scale, high-quality cybersecurity evaluation framework designed to rigorously assess the capabilities of AI agents on real-world vulnerability analysis tasks. · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/GLM-5.1">GLM-5.1</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mythos_AI">Mythos AI</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#AI`, `#Tencent`, `#open-source`, `#vulnerability discovery`

---