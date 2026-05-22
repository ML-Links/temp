# Chapter 1: Introduction


## Overall assessment

Chapter 1 has a strong structural backbone. The research problem is well grounded in literature, the three research questions are clearly stated and appropriate for the thesis scope, the contribution statement is specific and visible (Section 1.6), and the chapter structure overview (Section 1.8) is present. This is a disciplined and well-organised introduction overall.

The chapter has three issues that must be addressed. 

---

## What works well

- The problem statement (Section 1.2) is grounded in real literature, identifies the cross-domain gap clearly, and gives specific examples of why individual standards are insufficient.
- Research questions (Section 1.5) are precise and directly map to the three analytical workstreams (STRIDE → RQ2, standards gap → RQ3, framework design → RQ1).
- Objectives (Section 1.3) are stated as concrete deliverables, not as "to learn about."
- Scope and boundaries (Section 1.4) define what is and is not included. This is good Axiom 2 compliance.
- Contribution statement (Section 1.6) identifies six specific contributions, each with a clear description.
- Chapter structure (Section 1.8) is present, as required.

---

## Issues to address

### 1. Must Fix: Remove exact results from the introduction

**What is wrong:** Section 1.6 (Contribution Statement) includes highly specific quantitative outcomes: " 80 distinct threats", "94 3GPP, 53 NIST, 10 ISO/IEC, and 9 CSA CCM gaps", "A set of over thirty practical controls," and "the framework reduces the risk scores of the eight most critical threats by 40% to 75%." These are findings from Chapters 5 and 6, not introductory framing.

**Why it matters:** The introduction template explicitly forbids results in the introduction. Stating exact findings in Chapter 1 weakens the persuasive effect when the reader reaches those same numbers in Chapter 5 or 6, and it risks making the introduction sound like a summary rather than a framing chapter.

**How to fix it:** Keep the contribution categories but replace exact counts with type descriptions. For example:

> "A comprehensive, component-level threat catalog for the UAV-5G-cloud architecture ..."

> "A clause-level gap analysis of four major security frameworks ..."

> "A layered cybersecurity framework comprising controls across radio, edge, cloud, AI, and organizational domains, each mapped to the specific threats and gaps it mitigates."

The exact numbers can be reserved for Chapter 5 (STRIDE results, gap analysis results) and Chapter 6 (risk reduction table).

---

### 2. Must Fix: Shorten Section 1.7 (AI Anomaly Detection)

**What is wrong:** Section 1.7 is three substantial paragraphs covering AI deployment points, technical mechanisms, research challenges, and a list of specific controls (A-1 through A-6). This exceeds the scope of an introduction subsection and begins to function as a theoretical background or methodology section.

**Why it matters:** The introduction should state the thesis scope boundaries, not develop concepts. Extended technical discussion in the introduction slows the reader's entry into the research problem and belongs in Chapter 4.

**How to fix it:** Reduce Section 1.7 to one short paragraph that explains the scope boundary. For example:

> "AI anomaly detection is acknowledged in this thesis as a conceptual future-enhancement mechanism for monitoring telemetry deviations. Specific controls for prompt-injection prevention and model-provenance verification are included in the proposed framework. The design, training, and empirical validation of a production anomaly-detection system are beyond the scope of this study and are deferred to future work (Section 6.6)."

The current detailed content of 1.7 can be condensed into Chapter 4's AI/LLM section and the framework chapter.

---

### 3. Must Fix: Fix the factual inconsistency in Section 1.8 (chapter structure)

**What is wrong:** Section 1.8 describes Chapter 3 as presenting "the eight-phase mission communication flow." Chapter 3 actually describes **ten** sequential phases (Phases 1–10, as stated in Chapter 3: "ten sequential phases, as depicted in the sequence diagram").

**How to fix it:** Change "eight-phase" to "ten-phase" in the Chapter 3 description in Section 1.8. Also run a quick check across the introduction to confirm that all other counts (8 components, 10 phases, 3 research questions) are stated consistently.

---

### 4. Should Fix: Add a compact, explicit validation statement

**What is wrong:** The validation strategy is spread across Objective 6 ("validate through expert review and scenario analysis") and the scope section. There is no single sentence that clearly states how the thesis is validated.

**Why it matters:** The introduction expects the reader to understand how results are evaluated. 

**How to fix it:** Add one compact sentence in Section 1.3 or at the end of Section 1.6:

> "The framework was validated through attack-tree replay, structured expert review by two practitioners with 5G and UAV security backgrounds, and a Plausibility × Impact risk-scoring comparison of pre- and post-control threat profiles for the eight most critical threats."

---

### 5. Should Fix: Add a short limitations statement

**What is wrong:** Section 1.4 is a detailed scope section that says what is included. It does not contain a compact statement of what is *not* done, particularly: no live system testing, no physical testbed, no independent penetration testing, no full regulatory DPIA, no insider threat modeling.

**Why it matters:** A limitations statement in the introduction (not only in Section 6.5) prevents the reader from expecting more than the thesis delivers.

**How to fix it:** Add one paragraph at the end of Section 1.4 or as a short separate subsection 1.4.1 titled "Limitations":

> "The analysis is based on design review and supporting documentation, as no live penetration testing, physical testbed evaluation, or real-time monitoring was performed. The findings apply specifically to the DJI M350 RTK platform, the Elsight DroneCommX module, and the Microsoft Azure-hosted FlightHub 2; they may require adaptation for other platforms. Risk ratings are qualitative estimates derived from published threat intelligence rather than empirically measured probabilities. AI/ML controls are described at a conceptual level only, as no operational large language model was tested. These limitations are discussed further in Section 6.5."

---

### 6. Good to Consider: Review tense

The chapter is mostly in the correct thesis-report style (past tense for completed actions, present for established facts). 

A few isolated passages still carry plan-like wording (e.g., "This study aims to develop "). Run one final tense check to ensure the chapter reads as a completed study, not a proposal.
