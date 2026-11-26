---
layout: default
title: "Horizon Summary: 2026-11-26 (EN)"
date: 2026-11-26
lang: en
---

> From 34 items, 8 important content pieces were selected

---

1. [Scott Aaronson reacts to claim that the matrix multiplication exponent is exactly 9/4](#item-1) ⭐️ 9.0/10
2. [Anthropic's 17M-line GRH Lean proof compressed to 76k lines](#item-2) ⭐️ 9.0/10
3. [1Password Discloses Incident Where Compromised Employee Device Pushed Code to Backend](#item-3) ⭐️ 8.0/10
4. [Google Research Releases 'Cogentic' Papers on Integer Factorization and Discrete Logs](#item-4) ⭐️ 8.0/10
5. [Developer Audits Clojure's Core Library with Lean, Finds Unreported Bugs](#item-5) ⭐️ 8.0/10
6. [US closes loophole allowing remote access to advanced AI chips](#item-6) ⭐️ 8.0/10
7. [Minecraft Java 1.20.5+ Hit by High-Risk RCE via Malicious Fonts in Resource Packs](#item-7) ⭐️ 8.0/10
8. [Samsung and SK Hynix Said to Adopt YMTC's Xtacking 3D NAND Tech via Cross-Licensing](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Scott Aaronson reacts to claim that the matrix multiplication exponent is exactly 9/4](https://scottaaronson.blog/?p=10379) ⭐️ 9.0/10

Scott Aaronson published a post titled "Holy shit holy shit holy shit holy shit: The magnitude of what's now happening," reacting to an OpenAI preprint released on November 24 that claims the exponent of square matrix multiplication, ω, is exactly 9/4 over every field, backed by a Lean formalisation covering the division-free case. The post drew well over a thousand comments and became one of the most-discussed technical items of the week. If the claim holds, it would close a decades-old open problem in algebraic complexity by supplying a matching lower bound for the fast matrix multiplication upper bound that OpenAI itself announced in October, a result that would ripple through algorithm design and complexity theory. That the proof reportedly came from an AI lab rather than a human mathematician is what turns a niche theorem into a broader argument about how far AI's mathematical ability generalises — and, in Aaronson's framing, about whether other supposed hard problems might soon fall. The preprint credits no individual authors and names no model, and its Lean formalisation covers only the division-free case, so the full general-field statement rests on the prose argument rather than machine-checked proof. For context, the best known upper bounds had for years crept down toward roughly ω < 2.37 while the only universal lower bound remained the trivial 2, which is why a lower bound of 2.25 is the surprising half of the claim.

hackernews · Kotlopou · Nov 25, 19:11 · [Discussion](https://news.ycombinator.com/item?id=50646108)

**Background**: The matrix multiplication exponent ω is defined as the infimum of all exponents τ such that two n×n matrices can be multiplied using O(n^(τ+ε)) arithmetic operations for every ε > 0; the naive algorithm gives τ = 3 and Strassen's 1969 result first broke below it. Because a lower bound of 2 is trivial (any algorithm must at least read its inputs), the interesting question has always been how far the true value sits between 2 and the best upper bound, and pinning it exactly would settle the asymptotic complexity of one of computing's most fundamental operations. Aaronson's post also circles cryptography, since public-key systems rest on problems assumed to be genuinely hard — so a demonstration that AI can force a breakthrough on a long-open hardness question naturally raises the question of whether deployed crypto is safe.

<details><summary>References</summary>
<ul>
<li><a href="https://aitoolsrecap.com/Blog/openai-matrix-multiplication-exponent-nine-fourths">OpenAI Says Matrix Multiplication Stops at 9/4 | AIToolsRecap</a></li>
<li><a href="https://en.wikipedia.org/wiki/Computational_complexity_of_matrix_multiplication">Computational complexity of matrix multiplication - Wikipedia</a></li>
<li><a href="https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf">math/preprints/The-matrix-multiplication-exponent-is-nine ...</a></li>

</ul>
</details>

**Discussion**: Commenters split into several camps: one argues the big AI labs almost certainly do not yet hold working cryptanalytic breaks, since organizations that large leak and whistleblowers would surface anything that big. Others push back on extrapolation itself, noting that AI's fluency with axiomatic, a priori mathematics does not imply it will "solve" empirical fields or play the sci-fi role of destroying humanity. A third strand is meta: one commenter argues humans are biologically incapable of registering even a fraction of the appropriate alarm, while another invokes Bruno Latour's "centres of calculation" and Tycho Brahe's data-normalising work to suggest that organising knowledge, not raw proof power, is what actually enables scientific revolutions.

**Tags**: `#AI`, `#cryptography`, `#mathematics`, `#algorithms`, `#research-breakthroughs`

---

<a id="item-2"></a>
## [Anthropic's 17M-line GRH Lean proof compressed to 76k lines](https://github.com/lsernau/grh-lean) ⭐️ 9.0/10

A contributor (lsernau) published grh-lean on GitHub, a drastically compressed and human-documented rewrite of Anthropic's Lean formalization of the Generalized Riemann Hypothesis material, cutting the AI-generated proof from roughly 17 million lines down to about 76,000 lines — a 99.56% reduction. The repository also splits the development into a clearly labeled "known math" versus "new math" portion and adds explanatory documentation throughout. The result directly engages Terence Tao's recent critique that machine-generated formal proofs, however correct, are so large and opaque that they deliver no human insight. If giant AI-produced proofs can be golfed down by orders of magnitude and documented, formal verification becomes far more plausible as the trust layer for AI-generated mathematics and code. Beyond the raw line-count reduction, the repository's main value is structural: separating established results from newly formalized content and annotating the code in human-readable prose. The caveat is that 76k lines of tactic-style Lean is still far beyond what any person can check line by line, so actual trust continues to rest on Lean's small trusted kernel rather than on human reading.

hackernews · nb-t · Nov 25, 21:48 · [Discussion](https://news.ycombinator.com/item?id=50648050)

**Background**: Lean is an open-source proof assistant in which every proof step is checked by a small trusted kernel, so a formalization can be verified by machine even if no human reads it. The Generalized Riemann Hypothesis (GRH) extends the classical Riemann Hypothesis about zeros of the zeta function to a much broader class of L-functions, such as Dirichlet L-functions, and is one of the central open conjectures in analytic number theory. Anthropic produced a very large Lean development around GRH-related material, and this project is a human-curated, compressed re-presentation of that work rather than a new proof of the conjecture.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://agentconn.com/blog/verification-bottleneck-lean-trust-layer/">Lean Is Becoming AI 's Trust Layer - AgentConn Blog</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters praised the clear "known math" versus "new math" split and the pervasive documentation, saying it makes the development far easier to digest. Others asked whether LLM proof-golfing actually answers Tao's insight critique, or merely produces a smaller opaque object, and skeptics who looked at sample files wondered how realistically any human could read and grok the Lean code to confirm correctness.

**Tags**: `#formal-verification`, `#lean`, `#ai-for-math`, `#proof-compression`, `#riemann-hypothesis`

---

<a id="item-3"></a>
## [1Password Discloses Incident Where Compromised Employee Device Pushed Code to Backend](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

1Password published an update on a November 2026 security incident in which an employee's compromised device allowed a malicious actor to push code toward its backend services. The vendor's write-up describes the incident and lists remediation actions, but does not state whether GitHub branch protection rules were in place or were bypassed. 1Password is a widely used password manager, so any sign that code could reach its production services raises trust questions for millions of users who rely on it as a security boundary. The case also reinforces a broader industry pattern: endpoint compromise of an employee laptop is now the most common entry point into SaaS supply chains, affecting every company with privileged developer access. The announcement does not disclose whether branch protection rules, mandatory pull-request reviews, or required status checks were configured on the repositories involved, which is the key open question about how code reached production. 1Password does state that only a small number of users were in the affected state and were individually notified, and it notes that its end-to-end encrypted vault data remains protected by the underlying encryption design.

hackernews · lxhrstn · Nov 25, 17:18 · [Discussion](https://news.ycombinator.com/item?id=50644817)

**Background**: Branch protection rules in GitHub let a repository owner block force pushes and deletions to important branches like main, and require approvals or passing CI checks before any merge. When an attacker controls a developer's laptop, they inherit that developer's credentials and can attempt to push code directly, so these guardrails are the last line of defense between a phished endpoint and production. SaaS supply-chain attacks follow exactly this path: compromise an identity or device with deployment rights rather than attacking the software package itself, which is why identity and endpoint visibility matter as much as code review.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches">About protected branches - GitHub Docs</a></li>
<li><a href="https://www-theregister-com.nproxy.org/security/2026/05/15/openai-caught-in-tanstack-npm-supply-chain-chaos-after-employee-devices-compromised/5241019">OpenAI caught in TanStack npm supply chain chaos after employee ...</a></li>
<li><a href="https://appomni.com/blog/saas-supply-chain-attacks-mitre-attck-mapping/">SaaS Supply Chain Attacks : MITRE ATT&CK | AppOmni</a></li>

</ul>
</details>

**Discussion**: Commenters on Hacker News were largely critical of the disclosure's gaps rather than reassured by it. Security expert tptacek called the 'compromised employee laptop leads to pushed code' pattern the single most important attack vector for SaaS companies, noting that as headcount grows the probability of at least one compromised laptop approaches one, while others pressed on whether push-to-main was disabled and whether branch protection existed, and one user reported receiving a high-quality phishing email apparently built on the incident data.

**Tags**: `#security`, `#supply-chain`, `#saas`, `#password-managers`, `#incident-response`

---

<a id="item-4"></a>
## [Google Research Releases 'Cogentic' Papers on Integer Factorization and Discrete Logs](https://github.com/google-research/google-research/tree/master/cogentic_research_papers) ⭐️ 8.0/10

Google Research has published a collection of 'Cogentic' research papers in its google-research GitHub repository, covering integer factorization, discrete logarithms, and related computational number theory problems. The release drew a large Hacker News thread (roughly 481 points and 345 comments) dominated by debate over the cryptographic meaning of the results. Integer factorization and discrete logarithms are the hardness assumptions behind RSA, Diffie-Hellman, and ElGamal, so any claimed algorithmic progress against them attracts immediate scrutiny from cryptographers. The release also feeds a broader narrative that AI-assisted systems are starting to produce novel results in pure mathematics at a rapid pace. According to Hacker News commenter gukoff, the factorization result is layered on top of the general number field sieve (GNFS), which already has a far better asymptotic complexity than the new algorithm. Cogentic did not prove the three unproven heuristics GNFS relies on; instead it replaced the GNFS components that depend on them, paying a substantial complexity penalty, so this is not a practical break of deployed cryptosystems.

hackernews · rgwohlbold · Nov 25, 13:33 · [Discussion](https://news.ycombinator.com/item?id=50642086)

**Background**: Integer factorization is the problem of writing a composite number as a product of primes; many public-key schemes, most famously RSA, are built on the assumption that this is infeasible for large numbers. The discrete logarithm problem — finding the exponent x in g^x = h within a group — is the analogous hard problem underlying Diffie-Hellman key exchange and ElGamal encryption. The general number field sieve is the best known classical algorithm for factoring large integers, and both problems would be solvable in polynomial time on a sufficiently large quantum computer running Shor's algorithm.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Integer_factorization">Integer factorization - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Discrete_logarithm">Discrete logarithm - Wikipedia</a></li>
<li><a href="https://news.ycombinator.com/item?id=50642086">Google releases Cogentic papers on integer factorization , discrete ...</a></li>

</ul>
</details>

**Discussion**: Sentiment in the thread was a mix of excitement and skepticism: several commenters framed the result as part of a wave of AI-driven mathematical discovery (one comparing it to AlphaGo's exploration of Go's search space), while others noted the irony that dramatic research news keeps arriving as the AI market slides. The most substantive pushback came from gukoff, who argued the factorization advance is asymptotically inferior to GNFS and that the bar for accepting AI-generated proofs has risen sharply; another commenter cited credible rumors that this is 'the tip of something bigger.'

**Tags**: `#cryptography`, `#integer-factorization`, `#number-theory`, `#google-research`, `#ai-for-math`

---

<a id="item-5"></a>
## [Developer Audits Clojure's Core Library with Lean, Finds Unreported Bugs](https://s.conao3.com/blog/2026/e4f733) ⭐️ 8.0/10

A developer used the Lean proof assistant to analyze Clojure's core library (clojure.core) and reported a list of previously unreported bugs, publishing the findings in a blog post that reached the front page of Hacker News with 211 points and 73 comments. The work is notable for applying a dependently typed proof assistant to audit the core of a dynamically typed, JVM-hosted language rather than to verify a bespoke algorithm. Clojure's core library underpins a large production ecosystem — Nubank, which acquired Rich Hickey's Cognitect, runs substantial infrastructure on it — so finding latent edge-case bugs in primitives like `get` and Java-interop calls matters to many downstream users. More broadly, the experiment shows how proof-assistant tooling is drifting from pure mathematics and formal proofs into practical code auditing, raising questions about noise, false positives, and how such reports should be triaged. Commenters pushed back on at least two findings as false positives caused by type mismatch that ordinary type checking would have caught: `(.indexOf (seq (byte-array [1 2 3])) 2)` fails because the argument is a Long while byte arrays store bytes, and `(get "abc" 1.9)` fails because `get` coerces the key to an integer in the string context. This suggests the audit's value depends heavily on filtering noise, and that some reported "bugs" are really misuse of Java interop or intended coercion semantics rather than defects in Clojure itself.

hackernews · encyclopedism · Nov 25, 14:56 · [Discussion](https://news.ycombinator.com/item?id=50642939)

**Background**: Lean is an open-source programming language and proof assistant designed for writing correct, maintainable and formally verified code; it gained wide attention in 2021 when researchers used it to formalize a proof by Peter Scholze in condensed mathematics. Clojure is a Lisp dialect on the JVM whose `clojure.core` namespace supplies the bulk of the language's standard functions, and because Clojure is dynamically typed, many type errors only surface at runtime. Formal verification differs from ordinary static analysis: a static analyzer derives control- and data-flow facts from source code, while a proof assistant lets you state a property and machine-check a proof that it holds for all inputs — so applying Lean to an existing dynamic language's library requires modeling that library's semantics.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://lean-lang.org/">Lean Programming Language</a></li>
<li><a href="https://clojuredocs.org/clojure.core">clojure.core namespace | ClojureDocs - Community-Powered ...</a></li>

</ul>
</details>

**Discussion**: Sentiment was broadly positive about the effort but critical of its precision: one commenter flagged two false positives and argued such audits would be far more useful with less noise, while another pointed to their own similar audit that found dozens of issues in SBCL, Clozure CL and ACL2. Others noted that heavyweight Clojure users like Nubank would normally lead one to expect core primitives to be spotless, and one commenter asked whether Lean has now displaced Rocq (formerly Coq) for program verification and whether language models are simply better at writing Lean.

**Tags**: `#Clojure`, `#Lean`, `#formal-verification`, `#static-analysis`, `#programming-languages`

---

<a id="item-6"></a>
## [US closes loophole allowing remote access to advanced AI chips](https://t.me/zaihuapd/45361) ⭐️ 8.0/10

The US Commerce Department's Bureau of Industry and Security issued an interim final rule in mid-November that extends export controls on advanced AI chips and servers to remote access, so that overseas data centers cannot be used to circumvent restrictions on computing power. The rule also requires licenses for the reexport of AI chips to Indonesia, Malaysia, Singapore, Thailand and Brazil, and was reportedly drafted with leadership from the Treasury Department and the National Security Council. This closes what regulators saw as the biggest remaining gap in the chip control regime: a Chinese company could previously train frontier models on US-designed accelerators housed in a third country without any item ever crossing a controlled border. It directly affects cloud providers, data center operators and chip exporters, and further narrows the routes by which China can obtain advanced AI compute. The rule obliges data centers, foreign foundries and chip exporters to conduct robust due diligence on customers, including checking for direct or indirect ownership or control by persons in Country Group D:5 or Macau, and it accompanies the rescission of the earlier AI Diffusion Rule. Because it is an interim final rule, it takes effect largely immediately while BIS collects public comments before finalizing the text.

telegram · zaihuapd · Nov 25, 11:35

**Background**: Under the US Export Administration Regulations (EAR), a "reexport" is the shipment or transmission of a controlled item from one foreign country to another, as opposed to an export from the United States; controls traditionally attach to physical items and to specific technologies and software. Advanced AI accelerators have become the central bottleneck for training large models, so US policy has progressively tried to limit who can buy them and where they can be installed. The earlier AI Diffusion Rule attempted to govern global distribution of AI chips by country tiers, but it drew heavy criticism from industry and allies and is being replaced by this more targeted approach focused on remote and cloud access.

<details><summary>References</summary>
<ul>
<li><a href="https://www.federalregister.gov/documents/2026/11/19/2026-23529/addressing-remote-access-to-advanced-semiconductors">Addressing Remote Access to Advanced ... - Federal Register</a></li>
<li><a href="https://www.gtlaw.com/en/insights/2026/11/bis-interim-final-rule-targets-remote-access-to-advanced-semiconductors-rescinds-ai-diffusion-rule">BIS Interim Final Rule Targets Remote Access to Advanced ...</a></li>
<li><a href="https://www.orrick.com/en/Insights/2026/11/US-Government-Establishes-Export-Controls-to-Address-China-AI-Remote-Access-Concerns">U.S. Government Establishes Export Controls to Address China ...</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#export controls`, `#US policy`, `#semiconductors`, `#cloud computing`

---

<a id="item-7"></a>
## [Minecraft Java 1.20.5+ Hit by High-Risk RCE via Malicious Fonts in Resource Packs](https://github.com/bikini/minecraft2shell) ⭐️ 8.0/10

A proof-of-concept published on November 22, dubbed minecraft2shell, shows that a crafted TrueType font delivered through a server resource pack triggers a native out-of-bounds write in FreeType 2.14.3 and earlier, allowing arbitrary code execution on Windows clients running Minecraft Java Edition 1.20.5 through 1.21.10 and snapshots 26.1 through 26.4. Mojang has not shipped an official patch and still bundles lwjgl-freetype 3.4.3, so a community mitigation called m2sfix 1.0.0 was released on November 24 as a Java agent or mod that disables font hinting. Because resource packs are pushed automatically by servers, a player can be compromised simply by joining a malicious or hijacked multiplayer server, turning a routine action into a code-execution vector for a game with hundreds of millions of players. The lack of an official Mojang patch leaves Windows Java Edition users dependent on a third-party mod or on manually disabling server resource packs, which raises broader questions about how much trust the game places in downloadable client-side assets. The flaw is a native memory corruption in FreeType's TrueType hinting path, so it is not a Java sandbox escape per se but executes outside the JVM's memory-safety guarantees; 1.20.4 and earlier plus Bedrock Edition are reported as unaffected, and the impact is limited to Windows clients. Until a fix lands, the reporter advises adding no resource packs, setting the multiplayer server resource pack option to "Disabled", or installing the m2sfix 1.0.0 agent/mod.

telegram · zaihuapd · Nov 25, 12:46

**Background**: FreeType is the widely used open-source library that rasterizes fonts, and its TrueType hinting code executes instructions embedded in a font file to align glyphs to the pixel grid — a powerful but historically bug-prone attack surface. LWJGL's lwjgl-freetype bindings are what Minecraft Java Edition uses to render text, so a font shipped inside a resource pack is parsed by that native code inside the game process. Out-of-bounds write bugs of this class, such as CVE-2025-27363 in FreeType, allow an attacker to corrupt memory and redirect execution, which is why a font file can become an RCE primitive.

<details><summary>References</summary>
<ul>
<li><a href="https://nhimg.org/glossary/cve-2025-27363-freetype-out-of-bounds-write/">What Is CVE-2025-27363 (FreeType Out-of-Bounds Write)?</a></li>
<li><a href="https://freetype.org/freetype2/docs/hinting/hinting.html">FreeType Hinting</a></li>
<li><a href="https://javadoc.lwjgl.org/org/lwjgl/util/freetype/FreeType.html">FreeType ( LWJGL 3.4.2-snapshot)</a></li>

</ul>
</details>

**Tags**: `#Minecraft`, `#RCE`, `#FreeType`, `#Security Vulnerability`, `#Java`

---

<a id="item-8"></a>
## [Samsung and SK Hynix Said to Adopt YMTC's Xtacking 3D NAND Tech via Cross-Licensing](https://t.me/zaihuapd/45377) ⭐️ 8.0/10

Samsung Electronics and SK Hynix have reportedly agreed, through a cross-licensing arrangement, to adopt parts of Yangtze Memory Technologies' (YMTC) Xtacking stacking technology in their 3D NAND flash production. All three companies declined to comment on the report, which has not been officially confirmed. If confirmed, this would mark a notable reversal of the usual direction of memory IP flow, with Korean giants licensing process architecture from a Chinese challenger rather than the other way around. It could also accelerate adoption of wafer-bonding architectures across the 3D NAND industry as vertical stacking becomes harder to scale. Xtacking fabricates the memory cell array and the CMOS logic control circuitry on two separate wafers that are then bonded together, allowing each part to be produced and optimized independently. Omdia analysts note this lets a NAND maker build the array in-house while outsourcing the logic die to a foundry, potentially accessing more advanced process nodes.

telegram · zaihuapd · Nov 26, 05:30

**Background**: 3D NAND builds memory cells in vertical layers, and the industry has traditionally placed the CMOS control circuitry either beside the array (the conventional side-by-side layout) or beneath it (the CuA, or CMOS-under-Array, approach). YMTC's Xtacking, launched in 2018 and now in its 3.0 generation, instead bonds a separately fabricated CMOS wafer to the array wafer, which the company says enables faster interfaces and greater flexibility. Cross-licensing is an arrangement in which two or more patent holders grant each other rights to use their technologies, typically to avoid litigation and reduce transaction costs.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ymtc.com/cn/technicalintroduction.html">晶栈® Xtacking ®先进架构- 长 江 存 储</a></li>
<li><a href="https://developer.aliyun.com/article/1100149">长 江 存 储 YMTC Xtacking 技 术 演进与芯片级解密-开发者社区-阿里云</a></li>
<li><a href="https://wiki.mbalib.com/wiki/交叉许可">交叉许可 - MBA智库百科</a></li>

</ul>
</details>

**Tags**: `#3D NAND`, `#semiconductor manufacturing`, `#Xtacking`, `#cross-licensing`, `#memory technology`

---