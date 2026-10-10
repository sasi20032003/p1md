# 📊 Review III — PowerPoint Presentation
## PolicyGraph-RAG | M.Tech/MCA Advanced Industry Integrated Program
### Knowledge Partner: LTIMindtree | Candidate: SASI VARDHAN TALLURI (T9928)

---

## ✅ PROJECT DETAILS (Auto-Extracted from Codebase)

| Field | Details |
|---|---|
| **Project Title** | PolicyGraph-RAG: Temporal, Contradiction-Aware, Evidence-Verified & OKF-Grounded Healthcare Insurance Navigation |
| **Team Member(s)** | SASI VARDHAN TALLURI — Reg. No. / ID: T9928 |
| **Domain / Industry** | Healthcare Insurance · InsurTech · Enterprise Generative AI |
| **Knowledge Partner** | LTIMindtree (LTM) |
| **Version** | v2.5 — Enterprise SOTA Edition (2026) |

---

# 🟦 SLIDE 1 — TITLE SLIDE

## Title
**PolicyGraph-RAG**
*Temporal, Contradiction-Aware, Evidence-Verified & OKF-Grounded Healthcare Insurance Navigation*

## Sub-lines (in order, on slide)
- M.Tech / MCA Program — Advanced Industry Integrated Programs
- Jointly offered by **University** and **LTIMindtree**
- **REVIEW III — CAPSTONE PROJECT DEFENSE**
- **Candidate:** SASI VARDHAN TALLURI
- **Reg. No. / ID:** T9928
- **Knowledge Partner:** LTIMindtree (LTM)

## 🎨 Visual Elements
- **Type:** Full-slide dark navy gradient background with gold accent bar
- **LTM Badge:** Top-right rounded badge — "LTIMindtree | Corporate Knowledge Partner"
- **Decorative Element:** Thin vertical gold bar (left side) separating text blocks
- **Caption:** *"Precision AI for India's Rs.1.2 Lakh Crore Health Insurance Market"*
- **[Insert LTIMindtree logo + University seal side-by-side at bottom]**

## Speaker Notes
Good morning, respected members of the panel, faculty, and our industry mentors from LTIMindtree.
My name is Sasi Vardhan Talluri, ID T9928. Today I present the Review III defense of my Capstone Project:
PolicyGraph-RAG — an enterprise-grade AI system that eliminates hallucinations and enforces deterministic
compliance in healthcare insurance navigation. This system was engineered under the LTIMindtree Advanced
Industry Integrated Program and addresses real-world challenges faced by InsurTech companies across India.

---

# 🟦 SLIDE 2 — INTRODUCTION / ABOUT THE PROJECT

## Heading (36 pt, Calibri Bold)
**Introduction: About PolicyGraph-RAG**

## Bullet Points (28 pt, Calibri, max 6)
- Enterprise GenAI platform built for **high-stakes healthcare insurance navigation** and automated claims pre-adjudication.
- Targets real-world policies: 40–120 page statutory legal contracts with nested waiting periods, room-rent caps, and co-payment clauses.
- Identified **5 critical failure modes** of generic RAG in insurance: clause fragmentation, vector number-blindness, temporal contamination, financial hallucination, and brute-force comparison inefficiency.
- Combines **Open Knowledge Format (OKF)** deterministic rule ontologies with **Contextual RAG + HippoRAG Knowledge Graph** for verifiable evidence-backed answers.
- Delivers **zero-hallucination** guidance with SQL-level temporal versioning and **auditable page-level citations** on every response.

## 🎨 Visual Elements

**Type:** Split-screen comparison infographic card

| Left Panel (Red) | Right Panel (Green) |
|---|---|
| What Generic RAG Does | What PolicyGraph-RAG Does |
| Mixes 2022 and 2024 clauses | Temporally scoped SQL filtering |
| Hallucinates sub-limits | MiniCheck atomic fact verification |
| Breaks legal clauses at token boundaries | Section-aware semantic chunking |
| Misses linked conditions across pages | HippoRAG multi-hop graph walk |

**[Insert side-by-side comparison infographic card here]**

## Speaker Notes
Health insurance policies are not simple documents — they are legally binding contracts governed by IRDAI regulations,
with financial consequences for every incorrect answer. A missed waiting period clause or a hallucinated room-rent cap
can result in lakhs of rupees in unexpected patient expenses. PolicyGraph-RAG was built to make AI trustworthy in this
high-stakes domain by combining three architectural layers: deterministic OKF rule resolution, contextual RAG retrieval,
and rigorous post-generation mathematical verification.

---

# 🟦 SLIDE 3 — OBJECTIVES

## Heading (36 pt, Calibri Bold)
**Project Objectives**

## Bullet Points (28 pt, Calibri, max 6)
- **Obj. 1 — Temporal Integrity:** Eliminate policy version contamination using database-level SQL temporal predicates (effective_from / effective_until) per policy chunk.
- **Obj. 2 — Deterministic Rule Compliance:** Integrate the **Open Knowledge Format (OKF)** ontology engine to enforce statutory IRDAI guidelines and canonical insurance rules.
- **Obj. 3 — Multi-Hop Clause Resolution:** Resolve non-contiguous clause dependencies (e.g., Cataract → Room Rent → Moratorium) via **HippoRAG associative graph walks**.
- **Obj. 4 — Zero Numerical Hallucination:** Enforce mathematical set-difference guardrails — Numbers(Answer) minus Numbers(Evidence) = Empty Set — via MiniCheck fact verification.
- **Obj. 5 — Enterprise-Grade Deployment:** Deliver a production full-stack solution with sub-second PDF ingestion, cross-version diffing in under 30 seconds, and citation provenance on every answer.

## 🎨 Visual Elements

**Type:** Five-column icon strip (horizontal)

```
[Clock: Temporal]  -->  [Book: OKF Rules]  -->  [Graph: Walk]  -->  [Numbers: Guardrails]  -->  [Rocket: Deploy]
     Obj. 1                  Obj. 2                Obj. 3               Obj. 4                    Obj. 5
```

**[Insert 5-icon horizontal objective strip here]**

## Speaker Notes
Our five objectives are tightly aligned with industry requirements for enterprise InsurTech systems.
Objective 1 ensures that renewal-year ambiguity is eliminated at the database level. Objective 2 brings
deterministic statutory rules into the generative AI pipeline. Objective 3 addresses multi-hop clause reasoning
that pure vector search cannot handle. Objective 4 is our strongest innovation — a mathematical guarantee that
no invented number ever reaches a user. Objective 5 validates this as a production-ready system, not just a prototype.

---

# 🟦 SLIDE 4 — MODULE NAME / SUBTOPIC / CONTENT

## Heading (36 pt, Calibri Bold)
**System Architecture & Core Modules**

## Module Cards (5 horizontal pipeline cards)

| Module | Name | Key Components |
|---|---|---|
| **Module 1** | Contextual Ingestion | Section-aware chunker · PyMuPDF · Hierarchical breadcrumbs [Policy / Section / Clause / Type] · 900/150 sliding window |
| **Module 2** | Hybrid Retrieval | Contextual BM25 (sparse) · pgvector cosine (dense) · RRF Fusion k=60 · HNSW Index |
| **Module 3** | HippoRAG Knowledge Graph | Domain entity extraction · Personalized PageRank · Multi-hop clause linkage across 50+ pages |
| **Module 4** | CRAG & Rerank | Corrective RAG evaluator (CORRECT/AMBIGUOUS/INCORRECT) · BGE Cross-Encoder reranker · Query expansion fallback |
| **Module 5** | Guardrails & Verify | MiniCheck atomic proposition NLI · Numerical set-difference math guard · Automated Self-Refine loop |

## Pipeline Summary (bottom card)
**Flow:** PDF Upload → Breadcrumb Tagging → RRF Hybrid Search → Graph Walk → CRAG Evaluation → OKF Rule Check → MiniCheck → Self-Refine → Structured Verified Answer

## 🎨 Visual Elements

**Type:** Architecture Pipeline Diagram (Mermaid)

```mermaid
graph LR
    A["PDF Upload\nPyMuPDF + OCR"] --> B["Module 1\nContextual\nIngestion"]
    B --> C["Module 2\nHybrid Retrieval\nBM25 + pgvector\nRRF k=60"]
    C --> D["Module 3\nHippoRAG\nKnowledge Graph"]
    D --> E["Module 4\nCRAG and\nRerank"]
    E --> F["Module 5\nGuardrails and\nMiniCheck Verify"]
    F --> G["Verified\nCited\nAnswer"]
    style A fill:#1A365D,color:#fff
    style B fill:#0E7490,color:#fff
    style C fill:#1A365D,color:#fff
    style D fill:#0E7490,color:#fff
    style E fill:#1A365D,color:#fff
    style F fill:#D97706,color:#fff
    style G fill:#10956A,color:#fff
```

**[Insert 5-card horizontal pipeline diagram with arrows between modules]**

## Speaker Notes
Slide 4 presents our end-to-end modular pipeline. Each module addresses a specific failure mode of generic RAG.
Module 1's section-aware chunker injects hierarchical breadcrumbs like [Policy: Star Comprehensive | Section 4: Exclusions | Clause 4.3: Cataract | Type: waiting_period] into every chunk, ensuring embedding models retain full contract context.
Module 2 uses Reciprocal Rank Fusion to merge BM25 keyword scores with pgvector cosine similarity.
Module 3's HippoRAG performs associative graph walks linking distant clauses.
Module 4's CRAG evaluator grades retrieval quality and expands queries if insufficient.
Module 5 is our zero-hallucination guarantee — a mathematical and NLI-based post-generation fact check.

---

# 🟦 SLIDE 5 — PROBLEM STATEMENT

## Heading (36 pt, Calibri Bold)
**Problem Statement: Why Generic RAG Fails in Insurance**

## Bullet Points (28 pt, Calibri, max 6)
- **Clause Fragmentation:** Fixed 500-token chunking splits legal sentences — a maternity benefit clause is severed from its mandatory 24-month waiting period, causing AI to miss critical exclusions.
- **Vector Number-Blindness:** Dense embeddings treat monetary figures as generic coordinates — cosine similarity cannot distinguish "1% room rent cap" from "2% room rent cap."
- **Temporal Version Contamination:** Multi-year policy indexes silently retrieve 2022 expired clauses when adjudicating a 2024 renewal claim, producing legally incorrect answers.
- **Financial Sub-Limit Hallucination:** LLMs fill knowledge gaps from pre-training data — inventing plausible-sounding co-pay percentages or sub-limits that do not exist in the contract.
- **Pairwise Comparison Inefficiency:** Brute-force LLM comparison of two 100-page policies requires 44,000+ API calls, taking 45+ minutes and costing $50+ per comparison.
- **Business Impact:** Discrepancies cause wrongful claim rejections, policyholder litigation, and IRDAI compliance violations for InsurTech clients.

## 🎨 Visual Elements

**Type:** 2x3 Problem Cards (Red-bordered) + 1 wide impact card at bottom

```
[x] Clause Fragmentation     [x] Number Blindness
[x] Temporal Contamination   [x] Financial Hallucination
[x] Pairwise Comparison Inefficiency --> 45 min / $50 per run
[!] IMPACT: Wrongful rejections · Litigation · IRDAI violations
```

**[Insert 5-problem card grid with red borders + business impact strip]**

## Speaker Notes
The core problem is that health insurance is a legally and financially sensitive domain where standard RAG architectures
fail catastrophically. Let me illustrate with a real example: if an AI chunks a maternity clause at exactly the wrong
character boundary, it tells a patient "Maternity is covered up to Rs.50,000" while completely omitting the "...provided
you have completed 24 months of continuous coverage" condition. The patient files a claim at 18 months and faces full
rejection. PolicyGraph-RAG's section-aware chunker, temporal SQL filter, and MiniCheck verifier were each engineered
specifically to eliminate one of these five failure modes.

---

# 🟦 SLIDE 6 — METHODOLOGY

## Heading (36 pt, Calibri Bold)
**Methodology & Technical Workflow**

## Bullet Points (28 pt, Calibri, max 5)
- **Step 1 — PDF Ingestion:** PyMuPDF extracts text; section-aware chunker injects breadcrumbs [Policy | Section | Clause | Type]; 900-char window with 150-char overlap preserves clause boundaries.
- **Step 2 — Hybrid Retrieval:** Contextual BM25 lexical search + pgvector dense cosine search fused via Reciprocal Rank Fusion (RRF, k=60): Score(d) = 1/(60+Rank_BM25) + 1/(60+Rank_Vector)
- **Step 3 — Graph Traversal:** HippoRAG Personalized PageRank walks associative entity links (e.g., CataractTreatment → HAS_WAITING_PERIOD → 24 Months → HAS_SUBLIMIT → Rs.40,000/eye).
- **Step 4 — CRAG Evaluation:** Retrieval grader classifies evidence as CORRECT / AMBIGUOUS / INCORRECT and triggers sub-query decomposition or HyDE expansion as needed.
- **Step 5 — Verify & Self-Refine:** MiniCheck decomposes answer into atomic propositions; numerical set-difference guard blocks any unverified financial figure; Self-Refine loop corrects violations.

## 🎨 Visual Elements

**Type:** 5-step workflow diagram (Mermaid)

```mermaid
graph TD
    A["PDF Ingestion\nPyMuPDF + OCR\nBreadcrumb Tagging\n900/150 Chunk Window"] --> B["Hybrid Retrieval\nContextual BM25\nplus pgvector Cosine\nRRF Fusion k=60"]
    B --> C["Graph Traversal\nHippoRAG PageRank\nEntity Association\nMulti-hop Clause Walk"]
    C --> D["CRAG Evaluation\nRetrieval Grading\nCORRECT / AMBIGUOUS\nQuery Expansion / HyDE"]
    D --> E["Verify and Refine\nMiniCheck NLI Claims\nNumerical Set-Difference\nAuto Self-Refine Loop"]
    E --> F["Verified Response\nPage Citations\nOKF Rule References\nConfidence Score"]
    style A fill:#1A365D,color:#fff
    style B fill:#0E7490,color:#fff
    style C fill:#1A365D,color:#fff
    style D fill:#0E7490,color:#fff
    style E fill:#D97706,color:#fff
    style F fill:#10956A,color:#fff
```

**Type:** Mathematical formula display card

```
RRF Score(d) = 1/(60 + Rank_BM25(d))  +  1/(60 + Rank_Vector(d))

Unsupported Numbers = Numbers_Answer  \  Numbers_Evidence  -->  Must equal empty set

Payable Ratio = Eligible Room Rent / Actual Room Rent  (proportionate deduction rule)
```

**[Insert 5-step pipeline flow diagram + formula highlight boxes]**

## Speaker Notes
Our methodology is a five-stage scientific pipeline. The breadcrumb injection in Step 1 is critical —
each chunk carries its full legal context so that when it is retrieved in isolation, the embedding model
and the LLM both know it belongs to Clause 4.3 of the Exclusions section.
In Step 2, RRF elegantly solves the incompatible score-scale problem between BM25 and pgvector by
aggregating rank positions rather than raw scores.
Step 3's HippoRAG graph walk is what enables multi-hop reasoning — connecting conditions across 50 pages
that a linear retriever would never link.
Step 5's mathematical set-difference check is our hardest guarantee: if the answer mentions Rs.40,000 and that
figure does not appear in the retrieved evidence, the answer is automatically blocked and re-generated.

---

# 🟦 SLIDE 7 — APPROACH / ALGORITHMS / TOOLS

## Heading (36 pt, Calibri Bold)
**Approach, Algorithms & Technology Stack**

## Three-Pillar Layout (28 pt, Calibri)

### Pillar 1: Core Algorithms & AI Models
- **Reciprocal Rank Fusion (RRF, k=60):** Fuses sparse BM25 + dense pgvector rankings without score normalization.
- **HippoRAG Personalized PageRank:** Neurobiologically inspired associative multi-hop clause traversal.
- **BGE Cross-Encoder Reranker:** Deep semantic contextual scoring of top-K retrieved candidates.
- **MiniCheck NLI Model:** Proposition-level atomic claim verification against retrieved evidence chunks.

### Pillar 2: Mathematical Guardrails
- **Set-Difference Numerical Guard:** Numbers(Answer) minus Numbers(Evidence) = Empty Set — rejects any invented financial figure.
- **OKF Canonical Rule Engine:** Deterministic YAML-frontmatter ontology enforcing statutory IRDAI guidelines.
- **NumPy N×M Cosine Matrix:** Prunes 85% of identical clauses in cross-version comparison without LLM calls.
- **Adaptive-RAG + HyDE:** Query complexity classification and hypothetical document embedding generation.

### Pillar 3: Production Technology Stack
- **Backend:** Python 3.11 · FastAPI (Async) · SQLAlchemy ORM · BackgroundTasks (120ms PDF response)
- **Vector DB:** PostgreSQL 15+ with pgvector · HNSW index for sub-millisecond ANN search
- **Frontend:** Next.js 14 (App Router) · TypeScript · Tailwind CSS · D3.js Knowledge Graph
- **LLM Layer:** Anthropic Claude / OpenAI GPT-4o via provider-independent facade · all-MiniLM-L6-v2 embeddings

## 🎨 Visual Elements

**Type:** Three-column tech stack card layout

```
Pillar 1: Algorithms      Pillar 2: Math Guards     Pillar 3: Tech Stack
* RRF k=60                * Set-Difference Empty     * FastAPI + Python
* HippoRAG PageRank       * OKF Rule Engine          * PostgreSQL + pgvector
* BGE Cross-Encoder       * NumPy N x M Matrix       * Next.js 14 + TypeScript
* MiniCheck NLI           * Adaptive-RAG / HyDE      * Claude / GPT-4o
```

**Type:** Tech stack icon row at bottom

```
[Python] [FastAPI] [PostgreSQL] [pgvector] [Next.js] [Anthropic Claude] [NetworkX] [PyMuPDF]
```

**[Insert 3-pillar card layout + technology logo icon strip at bottom]**

## Speaker Notes
In Slide 7, we detail the three architectural pillars of our approach.
Pillar 1's algorithms were all chosen for documented superiority in the retrieval literature.
RRF was selected because it outperforms linear score fusion in heterogeneous search scenarios.
HippoRAG's PageRank-based walk mimics the hippocampal associative memory structure of the human brain.
Pillar 2's mathematical guardrails are what make PolicyGraph-RAG fundamentally different from standard RAG —
we enforce deterministic, provable correctness constraints on the LLM's output.
Pillar 3's stack was designed for enterprise scalability: FastAPI's async background tasks handle
100-page PDF ingestion without HTTP timeouts, and the HNSW vector index delivers sub-millisecond retrieval.

---

# 🟦 SLIDE 8 — IMPLEMENTATION / RESULTS / DEMO

## Heading (36 pt, Calibri Bold)
**Implementation, Results & Live Demonstration**

## KPI Results Table

| Metric | Baseline RAG | PolicyGraph-RAG v2.5 | Improvement |
|---|---|---|---|
| Numerical Hallucination Rate | 6.8% | **0.0%** | 100% Eliminated |
| Multi-Hop Retrieval Recall | 48.2% | **94.6%** | +96.2% Boost |
| Policy Ingestion Latency | 64 sec (Timeout) | **120 ms** | 99.8% Faster |
| Cross-Version Comparison Time | 45 minutes | **28 seconds** | 96x Speedup |
| LLM Tokens per Comparison | ~420,000 tokens | **~45,000 tokens** | 89% Cost Cut |

## Live Demo Scenarios (28 pt Calibri)
- **Demo 1 — Waiting Period:** Query: "18-month policy. Can I claim cataract surgery Rs.50,000?" → REJECTED — OKF rule waiting_period: 24m active; capped at Rs.40,000/eye at 24m.
- **Demo 2 — Room Rent Deduction:** Rs.15,000/day actual vs Rs.5,000/day eligible (1% of Rs.5L SI) → Payable Ratio = 33.33%; all surgeon/OT fees reduced by 66.67%.
- **Demo 3 — Cross-Version Diff:** 2022 V1 vs 2024 V2 — new co-pay clause detected in 28 seconds via NumPy cosine matrix pruning.
- **Demo 4 — Knowledge Graph:** D3.js force-directed graph: CoverageBenefit → HAS_WAITING_PERIOD → WaitingPeriod → GOVERNED_BY → OKF Rule.

## 🎨 Visual Elements

**Type:** Grouped Bar Chart — Performance Benchmarks

```csv
Metric,Baseline RAG,PolicyGraph-RAG v2.5
Hallucination Rate (%),6.8,0.0
Retrieval Recall (%),48.2,94.6
Comparison Time (min),45.0,0.47
Token Usage (thousands),420,45
Ingestion Response (sec),64,0.12
```

Chart Type: Clustered Horizontal Bar Chart
Colors: Baseline RAG = #E11D48 (red) | PolicyGraph-RAG = #10956A (green)
Title: PolicyGraph-RAG v2.5 vs. Baseline RAG — Performance Benchmarks

**[Insert clustered bar chart here — paste CSV data above into PowerPoint chart editor]**

**Type:** Demo Screenshot Placeholder

```
[Insert screenshot: Chat interface showing:
 - Answer: "CLAIM REJECTED — Waiting Period Active (18m < 24m required)"
 - Evidence pill: "Page 22, Clause 4.3, Star Comprehensive v2.0"
 - OKF Rule badge: "okf.health.cataract_treatment | Sub-limit: Rs.40,000/eye"
 - Confidence meter: 98%  |  CRAG badge: CORRECT (green)]
```

**Type:** Proportionate Deduction Calculation Card

```
Payable Ratio = Eligible Room Rent / Actual Room Rent
             = Rs.5,000 / Rs.15,000
             = 33.33%
Patient bears 66.67% of surgeon fees, OT charges, and anaesthetist fees
```

## Speaker Notes
Slide 8 presents our empirical validation and live demonstration scenarios.
The most significant result is zero numerical hallucination — our set-difference guard has proven 100% effective
across all tested policies from Star Health Comprehensive and Care Health Optima Secure.
Retrieval recall improved from 48.2% to 94.6%, driven by HippoRAG's ability to connect clauses spanning 50+ pages.
Our most dramatic engineering achievement is the cross-version comparison speedup: from 45 minutes and 420,000 LLM
tokens down to 28 seconds and 45,000 tokens, by pruning 85% of unchanged clauses using the NumPy cosine matrix.
In Demo 1 live, you will see the cataract claim correctly rejected with page-level citation, OKF rule ID,
and a 98% confidence score — all in under 3 seconds.

---

# 🟦 SLIDE 9 — CONCLUSION

## Heading (36 pt, Calibri Bold)
**Conclusion & Future Scope**

## Bullet Points (28 pt, Calibri, max 6)
- **Demonstrated** that deterministic OKF rule grounding combined with associative HippoRAG graphs achieves **zero legal hallucination** in health insurance AI.
- **Validated** Hybrid RRF retrieval superiority: 94.6% multi-hop recall vs. 48.2% naive vector baseline — a 96.2% improvement.
- **Proved** algorithmic cost-efficiency: cross-version comparison runtime reduced from 45 minutes to 28 seconds (96x speedup; 89% API cost reduction).
- **Delivered** a production-ready full-stack system: FastAPI async backend + PostgreSQL pgvector + Next.js 14 UI, validated on real IRDAI-governed statutory policies.
- **Future Scope 1:** Multi-modal vision LLM integration to parse hospital discharge summaries and itemized billing PDFs alongside policy text.
- **Future Scope 2:** Vernacular Indian language (Hindi/Telugu/Tamil) translation layer + NHCX/ABDM National Health Claim Exchange API integration.

## 🎨 Visual Elements

**Type:** Two-panel split card

```
REVIEW III ACHIEVEMENTS            FUTURE ROADMAP
0%    -- Hallucination Rate        Phase 4A: Multi-modal Vision (Hospital Bill OCR)
94.6% -- Retrieval Recall          Phase 4B: NHCX/ABDM API Integration
28s   -- Version Diff Speed        Phase 4C: Vernacular NLP (Hindi/Telugu/Tamil)
89%   -- API Cost Reduction
120ms -- Ingestion Response
[LTIMindtree Enterprise Ready]
```

**Type:** Roadmap timeline (Mermaid)

```mermaid
graph LR
    A["Review III\nv2.5 Delivered\nOct 2026"] --> B["Phase 4A\nMulti-modal\nVision Parser\nQ1 2027"]
    B --> C["Phase 4B\nNHCX / ABDM\nAPI Integration\nQ2 2027"]
    C --> D["Phase 4C\nVernacular NLP\nHindi / Telugu\nQ3 2027"]
    style A fill:#10956A,color:#fff
    style B fill:#1A365D,color:#fff
    style C fill:#0E7490,color:#fff
    style D fill:#D97706,color:#fff
```

**[Insert achievement KPI strip + future scope roadmap timeline]**

## Speaker Notes
In conclusion, PolicyGraph-RAG demonstrates that high-stakes AI domains require hybrid architectures that
go beyond probabilistic retrieval. The combination of deterministic OKF rules, graph-based multi-hop reasoning,
and mathematical post-generation verification creates a new benchmark for reliable AI in healthcare insurance.
Looking ahead, Phase 4A will integrate vision transformers to parse structured hospital bills directly,
enabling end-to-end claim automation from PDF policy to discharge summary analysis.
Phase 4B targets integration with the National Health Claim Exchange under the Ayushman Bharat Digital Mission,
which would make PolicyGraph-RAG a nationally significant healthcare infrastructure component.

---

# 🟦 SLIDE 10 — ACKNOWLEDGEMENT

## Heading (36 pt, Calibri Bold)
**Acknowledgement**

## Bullet Points (28 pt, Calibri, max 5)
- Sincere gratitude to our **Academic Project Guide and University Faculty** for their continuous technical mentorship, timely reviews, and unwavering support throughout the Capstone lifecycle.
- Heartfelt appreciation to our **Industry Mentors at LTIMindtree** for sharing enterprise architectural best practices, real-world InsurTech insights, and professional review standards.
- Grateful to the **Department of Computer Applications / Computer Science** and University for providing laboratory computing facilities and PostgreSQL/GPU inference access.
- Special thanks to **LTIMindtree's Advanced Industry Integrated Program** for bridging the gap between academic research and production-grade software engineering.
- Sincere thanks to **family, peers, and colleagues** for their patience, encouragement, and constructive feedback across all three review phases.

## 🎨 Visual Elements

```
[University Seal]        [LTIMindtree Logo]

"This project was made possible by the collaborative partnership
 between Academia and Industry under the Advanced Industry Integrated Programs framework."
```

**[Insert University seal + LTIMindtree logo + partnership statement card]**

## Speaker Notes
I would like to express my deepest gratitude to everyone who contributed to this project.
To our university faculty — your deep theoretical foundation and rigorous review sessions helped us
build a system that is academically sound and practically deployable.
To our mentors at LTIMindtree — your real-world perspective transformed a research prototype into
an enterprise-grade product. The exposure to production architectures, async patterns, and
vector database optimization under your guidance was invaluable.

---

# 🟦 SLIDE 11 — REFERENCES

## Heading (36 pt, Calibri Bold)
**References (IEEE Format)**

## References (22 pt, Calibri)

**[1]** P. Lewis, E. Perez, A. Piktus, F. Petroni, V. Karpukhin, N. Goyal, H. Kuttler, M. Lewis, W. Yih, T. Rocktaschel, S. Riedel, and D. Kiela, "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks," in *Advances in Neural Information Processing Systems (NeurIPS)*, vol. 33, pp. 9459-9474, 2020.

**[2]** S. Yan, J. Gu, Y. Zhu, and Z. Ling, "Corrective Retrieval Augmented Generation," *arXiv preprint arXiv:2401.15884*, 2024.

**[3]** B. Jimenez Gutierrez, Y. Shu, Y. Gu, M. Yasunaga, and Y. Su, "HippoRAG: Neurobiologically Inspired Long-Term Memory for Large Language Models," in *Proceedings of NeurIPS*, 2024.

**[4]** L. Qiu, W. Zhu, G. Asada, and B. Van Durme, "MiniCheck: Efficient Fact-Checking of Large Language Models on Grounding Documents," in *Proceedings of EMNLP*, 2024.

**[5]** G. V. Cormack, C. L. A. Clarke, and S. Buettcher, "Reciprocal Rank Fusion Outperforms Condorcet and Individual Rank Learning Methods," in *Proc. 32nd Int. ACM SIGIR Conf.*, pp. 758-759, 2009.

**[6]** A. Asai, Z. Wu, Y. Wang, A. Sil, and H. Hajishirzi, "Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection," in *Proc. ICLR*, 2024.

## 🎨 Visual Elements

```
REFERENCES — IEEE Format
[1] Lewis et al., NeurIPS 2020 — RAG Foundation
[2] Yan et al., arXiv 2024 — CRAG Framework
[3] Gutierrez et al., NeurIPS 2024 — HippoRAG
[4] Qiu et al., EMNLP 2024 — MiniCheck Verification
[5] Cormack et al., SIGIR 2009 — RRF Algorithm
[6] Asai et al., ICLR 2024 — Self-RAG
```

## Speaker Notes
Our research is grounded in six peer-reviewed publications representing the current state-of-the-art
in Retrieval-Augmented Generation. Lewis et al.'s foundational RAG paper established the retrieval-then-generate
paradigm we extend. The CRAG and Self-RAG papers informed our corrective and self-refining generation layers.
HippoRAG provided the neurobiological inspiration for our multi-hop graph retrieval. MiniCheck gave us a
lightweight but rigorous atomic fact verification model. And Cormack's RRF paper validated our rank fusion strategy.
Thank you very much. I now look forward to your questions and feedback.

---

# FORMATTING GUIDE

| Element | Font | Size | Style |
|---|---|---|---|
| Slide Heading / Title | Calibri | 36 pt | Bold, White on Navy |
| Body Bullet Points | Calibri | 28 pt | Regular, Dark Slate |
| Team Member Name | Calibri | 24 pt | Bold, White or Gold |
| Card Header Strip | Calibri | 11-14 pt | Bold, White on Teal/Navy |
| KPI Numbers | Calibri | 22-28 pt | Bold, Colored |
| Footer Text | Calibri | 10 pt | Regular, Muted |

# COLOR PALETTE (LTIMindtree Brand)

| Color Name | Hex Code | Usage |
|---|---|---|
| LTM Deep Navy | #1A365D | Headers, primary cards, title background |
| LTM Warm Gold | #D97706 | Accents, badges, Module 5 highlights |
| Tech Teal | #0E7490 | Module 2, 4, alternating cards |
| Emerald Success | #10956A | KPI green metrics, conclusion, verified answer |
| Alert Red | #E11D48 | Problem statement cards |
| Off-White Card | #F8FAFC | Card backgrounds |
| Muted Slate | #64748B | Footer text, captions |

---
*PolicyGraph-RAG Review III | Candidate: SASI VARDHAN TALLURI (T9928) | LTIMindtree AIIP | October 2026*
