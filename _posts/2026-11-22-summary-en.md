---
layout: default
title: "Horizon Summary: 2026-11-22 (EN)"
date: 2026-11-22
lang: en
---

> From 23 items, 5 important content pieces were selected

---

1. [Lean Formal Verification of Riemann Hypothesis Sparks Trust and AI Debate](#item-1) ⭐️ 9.0/10
2. [GPGME Remote Code Execution Flaw Affects All Versions Before 2.3.0](#item-2) ⭐️ 8.0/10
3. [Microsoft Brings RDMA over USB4 to Windows, Letting Multiple PCs Run One Local AI Model](#item-3) ⭐️ 8.0/10
4. [Zhejiang University Demonstrates First On-Hardware QRAM on Superconducting Chip](#item-4) ⭐️ 8.0/10
5. [US Commerce to Finalize Rule Blocking Chinese AI Firms' Remote Chip Access](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Lean Formal Verification of Riemann Hypothesis Sparks Trust and AI Debate](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 9.0/10

A Lean community blog post announced a formal verification of the Riemann Hypothesis, reportedly also confirming the Generalized Riemann Hypothesis, with Anthropic mathematician Levent Alpöge saying Claude helped formalize large portions of modern mathematics and that the detailed proof manuscript exceeds 250,000 pages. If the verification holds, this would be a paradigm-shifting result for mathematics and formal methods, showing that AI-assisted formalization can tackle foundational problems and potentially reshaping how proofs are checked and trusted. The claim rests on Lean's kernel and independent checkers; commenters note that a fake Collatz refutation previously exploited a Lean kernel bug, but multiple independent implementations and consistency proofs make a bug affecting both the GRH proof and all kernels far less likely. The proof is encoded in Lean rather than presented as a conventional paper proof, and the 250,000-page manuscript plus Claude's involvement make independent checking and expert review central.

hackernews · g-b-r · Nov 21, 14:36 · [Discussion](https://news.ycombinator.com/item?id=50589618)

**Background**: Lean is an open-source proof assistant and functional programming language based on dependent type theory, used to encode mathematical definitions, statements, and proofs so they can be machine-checked. Formal verification means a proof is checked by a small trusted kernel rather than by human reviewers alone. The Riemann Hypothesis, posed by Bernhard Riemann in 1859, concerns the distribution of prime numbers and is one of mathematics' most famous open problems; its generalization, GRH, extends the conjecture to broader classes of L-functions.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_theorem_prover">Lean theorem prover</a></li>
<li><a href="https://lawrencecpaulson.github.io/2026/07/30/Collatz.html">Why is it all in the kernel ?</a></li>

</ul>
</details>

**Discussion**: Commenters are broadly impressed but cautious: some argue multiple independent kernels and consistency proofs make a kernel-bug explanation vanishingly unlikely, while others recall the fake Collatz refutation and stress that checkers are not fully independent. Several credit Levent Alpöge for expert guidance and see the AI-assisted formalization of large swaths of modern math as a major result in its own right.

**Tags**: `#formal-verification`, `#lean`, `#riemann-hypothesis`, `#mathematics`, `#ai-assisted-proofs`

---

<a id="item-2"></a>
## [GPGME Remote Code Execution Flaw Affects All Versions Before 2.3.0](https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) ⭐️ 8.0/10

A remote code execution vulnerability in GPGME, the C library interface to GnuPG, was publicly disclosed on 2026-11-20 and affects every version prior to 2.3.0. The flaw was discovered by Johan Carlsson and reported to the GPGME maintainers by GitLab on 2026-11-12, with the coordinated disclosure date pulled forward from 2026-11-25 to 2026-11-20 because GitLab had to ship an early fix alongside its Ruby2Shell update. GPGME is linked — dynamically, as a DLL, or statically — into an enormous range of software, including Gpg4win, GnuPG Desktop, most mail clients, many XMPP clients, Samba, and Flatpak, so a single flaw ripples across a very broad downstream ecosystem. GitLab's support for signed commits made code execution on that path particularly dangerous, and downstream packagers must now audit which bundled copies of the library they ship. Commenters point out that the underlying defect is a double free rather than a complete RCE chain, suggesting the "remote code execution" label may overstate practical exploitability. Notably, Red Hat appears to have patched the bug downstream roughly five years earlier based on output from conventional static-analysis tooling, while upstream GPGME missed it.

hackernews · gdgghhhhh · Nov 21, 08:32 · [Discussion](https://news.ycombinator.com/item?id=50587208)

**Background**: GPGME, short for "GnuPG Made Easy", is a C library that gives applications a stable programming interface for cryptographic operations performed by engines such as GnuPG or GpgSM, so programs do not have to invoke the gpg binary themselves. Because it is written in C, defects such as double frees and buffer overflows fall into the memory-safety class: they can corrupt memory and, in the worst case, be steered into arbitrary code execution. Coordinated vulnerability disclosure is the practice in which a reporter privately notifies the maintainer and a fix plus public advisory are released on an agreed schedule, which is why the GitLab-driven date change mattered here.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/gpg/gpgme">GitHub - gpg/gpgme: GnuPG Made Easy. NOTE: Maintainers are ...</a></li>
<li><a href="https://www.gnupg.org/documentation/manuals/gpgme/">Top (The ‘GnuPG Made Easy’ Reference Manual)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Memory_safety">Memory safety - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters pushed back on the headline framing, with one stating flatly that "it's a double free bug, not an RCE chain" and asking whether such reports are intentionally overstated. Others mapped the downstream blast radius — Samba, mail and XMPP clients, Flatpak, Gpg4win — and asked whether tools like apt are affected, while another used the episode to argue that humans should not be writing C/C++ without Rust-level tooling to prevent such bugs.

**Tags**: `#security`, `#vulnerability`, `#gnupg`, `#memory-safety`, `#open-source`

---

<a id="item-3"></a>
## [Microsoft Brings RDMA over USB4 to Windows, Letting Multiple PCs Run One Local AI Model](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 8.0/10

Microsoft released a developer preview of RDMA over USB4 on Windows that lets multiple PCs pool their memory and GPU compute over ordinary USB4 cables to run a single local AI model, with no dedicated network cards or switches required. In the demo, three AMD Ryzen AI Max+ 395 systems ran Qwen3-235B-A22B at 4-bit quantization at roughly 18.5 tokens per second, and the feature is being rolled out through Windows Insider. This turns a handful of ordinary Windows machines into a small inference cluster using ports and cables people already own, which could let enthusiasts and small teams run models far larger than any single consumer PC's memory could hold. It also signals Microsoft building distributed local-AI infrastructure directly into Windows, an alternative to renting cloud GPUs or buying workstation-class hardware. The capability is a developer preview rather than a finished feature, so it ships first to Windows Insider testers and should be treated as experimental. Reported comparisons suggest the USB4 path offers significantly lower latency than Ethernet-based setups over the same USB4 link, but the pooled memory and interconnect bandwidth still fall far short of datacenter fabrics, and the ~18.5 token/s result was achieved only with aggressive 4-bit quantization.

telegram · zaihuapd · Nov 21, 06:13

**Background**: RDMA (Remote Direct Memory Access) lets one machine read and write another machine's memory directly, bypassing much of the CPU and operating-system overhead that ordinary networking incurs; it has long been a staple of datacenter fabrics such as InfiniBand and RoCE. USB4 tunnels PCIe and offers high bandwidth over a cheap, ubiquitous cable, which makes it a plausible carrier for RDMA between consumer PCs. The model used in the demo, Qwen3-235B-A22B from Alibaba's Qwen team, is a mixture-of-experts model with 235 billion total parameters but only about 22 billion active per token, so it needs enormous total memory but relatively modest compute. Quantizing weights to 4-bit shrinks that memory footprint by roughly 75% versus 16-bit, which is what makes spanning the model across several machines practical.

<details><summary>References</summary>
<ul>
<li><a href="https://techcommunity.microsoft.com/blog/microsoftusbblog/introducing-rdma-over-usb4®-on-windows-run-larger-local-ai-models-across-pcs/4574602">Introducing RDMA over USB4® on Windows: run larger local AI ...</a></li>
<li><a href="https://windowsreport.com/windows-pcs-can-now-team-up-over-usb4-to-run-ai-models-that-wont-fit-on-one-machine/">Windows PCs Can Now Team Up Over USB4 to Run AI Models That ...</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3-235B-A22B">Qwen/Qwen3-235B-A22B · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#Microsoft`, `#USB4`, `#RDMA`, `#local AI`, `#distributed inference`

---

<a id="item-4"></a>
## [Zhejiang University Demonstrates First On-Hardware QRAM on Superconducting Chip](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 8.0/10

Zhejiang University researchers reported the first experimental demonstration of a quantum random access memory (QRAM) on their self-developed superconducting chip 'Tianmu-2,' fetching 4-bit and 8-bit data with 80.9% and 60.4% accuracy, respectively, with results published in Nature Physics. QRAM is a foundational component for loading classical data into quantum superpositions and is considered a prerequisite for many quantum algorithms to achieve speedups, so a working hardware prototype marks a step from theoretical proposal to experimental reality. However, the sharp accuracy drop at 8 bits shows that scalable, fault-tolerant QRAM remains a major engineering challenge. The prototype reduced circuit depth by more than 30% versus an unoptimized implementation and showed partial noise resilience, while the 80.9% to 60.4% accuracy drop from 4-bit to 8-bit fetching illustrates how errors accumulate as address and data widths grow. The team says next steps focus on scaling up QRAM.

telegram · zaihuapd · Nov 21, 08:31

**Background**: A quantum random access memory (QRAM) uses qubits to address memory cells in quantum superposition, allowing a quantum computer to retrieve data in a way that can feed algorithms such as quantum search or linear-systems solvers. The concept was formalized in 2008 with an architecture requiring O(log N) switches rather than N, but building it physically has remained difficult. Superconducting qubits, the technology behind chips like Tianmu-2, are one of the leading platforms for quantum hardware and operate at cryogenic temperatures.

<details><summary>References</summary>
<ul>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC10490729/">Quantum Random Access Memory for Dummies - PMC</a></li>
<li><a href="https://link.aps.org/doi/10.1103/PhysRevLett.100.160501">Quantum Random Access Memory | Phys. Rev. Lett.</a></li>
<li><a href="https://baike.baidu.com/en/item/Tianmu-2/4929794">Tianmu-2_Baiduwiki - 百度百科</a></li>

</ul>
</details>

**Tags**: `#quantum computing`, `#QRAM`, `#superconducting qubits`, `#hardware research`, `#Nature Physics`

---

<a id="item-5"></a>
## [US Commerce to Finalize Rule Blocking Chinese AI Firms' Remote Chip Access](https://t.me/zaihuapd/45289) ⭐️ 8.0/10

The US Commerce Department is finalizing a rule that would prevent Chinese AI companies from remotely accessing advanced AI chips hosted in overseas data centers, with publication possible as early as this month. The rule would extend existing semiconductor export restrictions to seven additional countries, including Malaysia, Singapore and Thailand, in an effort to close remote-access and chip-smuggling loopholes, and is being finalized after consultations with other government agencies. This closes one of the largest remaining gaps in US chip export controls: Chinese firms could previously rent compute in third countries instead of buying restricted hardware directly. It could significantly reshape global AI compute availability for Chinese model developers, and it directly affects NVIDIA, which has argued that restricting overseas deployments undermines the global reach of US AI infrastructure. The rule is reported to cover seven countries beyond the current restrictions, with Malaysia, Singapore and Thailand named, and the White House has already asked Congress to legislate that Commerce draft it. NVIDIA lobbied against closing the remote-access gap, and the report originates from The Information, with the exact scope, thresholds and effective date not yet public.

telegram · zaihuapd · Nov 22, 04:34

**Background**: Since 2022 the US has progressively restricted exports of advanced AI accelerators such as NVIDIA's high-end GPUs to China, requiring licenses for sales to Chinese buyers. Because these controls attach to the physical shipment of hardware, firms could partly sidestep them by renting compute from data centers in countries not covered by the restrictions — the so-called remote-access loophole. Southeast Asian countries have become key transit and hosting hubs for such capacity, which is why the new rule targets them specifically.

**Tags**: `#AI chips`, `#export controls`, `#geopolitics`, `#semiconductors`, `#NVIDIA`

---