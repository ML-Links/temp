# Chapter 6: Discussion and Conclusions

## Overall assessment

Chapter 6 contains a large amount of substantive work: a comprehensive 5-layer framework with 30+ controls, a risk-reduction table, structured answers to all three research questions, a detailed limitations section, and a future research directions section. The effort is visible and the analytical depth is appropriate for a master thesis.

The structural problem is that this chapter introduces the main contribution (the cybersecurity framework) for the first time. The results chapter (Chapter 5) leads up to the framework analysis but stops before presenting it. This means the thesis currently has its results and discussion chapters in the wrong order: analysis in Chapter 5, contribution in Chapter 6. 

A secondary issue is language calibration. Several sentences use verbs and framing that imply operational deployment ("security is achieved," "rogue gNB attacks are neutralized"), which overstates what an analytical-design study can conclude.

---

## What works well

- The five-layer framework structure (Radio/5G, Edge Device, Cloud Platform, AI/LLM, Organizational/Privacy) is logical and comprehensive.
- Each control has a unique identifier, a description, a technical implementation note, and a list of threats/gaps it mitigates. This is exactly the right level of detail.
- The residual risks table (Table 6.1) is present and appropriately acknowledges what the framework cannot fully address.
- The risk-reduction table (Table 6.2) is present and quantifies the improvement, with percentage reductions.
- The limitations section (6.5) is appropriately detailed and honest.
- The future research directions section (6.6) gives a credible research agenda.
- The research questions are answered directly in Section 6.7, which is exactly what is required.

---

## Issues to address

### 1. Move the framework definition to Chapter 5 and repurpose Chapter 6 as pure discussion

**What is wrong:** Sections 6.2.1 through 6.2.5 introduce the proposed cybersecurity framework and all its control definitions for the first time. This is the original contribution of the thesis. According to the university's templates, the original contribution belongs in the Results and Analysis chapter. The Discussion chapter should interpret, evaluate, and reflect on results already presented, not introduce new technical artifacts.

**How to fix it:**

1. Move Sections 6.2.1–6.2.5 (the complete control framework) into Chapter 5 as a new final section (e.g., Section 5.5 "Proposed Layered Cybersecurity Framework"). Also move Table 6.2 (risk reduction scores) into the same Chapter 5 section, as it is the immediate validation of the framework.

2. Revise Chapter 6 so it begins with a reference to the framework presented in Chapter 5:
> *"Chapter 5 presented the proposed layered cybersecurity framework ... This chapter evaluates the framework's effectiveness..."*

3. Keep in Chapter 6: Table 6.1 (residual risks), Section 6.3 (key findings, rephrased as discussion rather than introduction), Section 6.5 (limitations), Section 6.6 (future work), and Section 6.7 (research questions answered).

---

### 2. Calibrate language to match the analytical (non-deployment) validation level

**What is wrong:** Several sentences in Chapter 6 use language that implies operational deployment or empirical proof:

- *"Security is achieved through a layered defense-in-depth architecture..."* (Section 6.7, RQ1 answer) this implies operational fact, not analytical conclusion.
- *"Rogue gNB attacks are neutralized by application-layer encryption with HMAC-based integrity (R-1)."* (Section 6.3.1)  "neutralized" implies complete elimination; the thesis has no live testing to support this.
- *"JWT theft is mitigated by short-lived, session-bound tokens (C-1). A stolen token cannot be used on an unauthorized device."*  "cannot be used" is a claim that can only be proven by testing.
- *"SQL injection and XSS are blocked by the WAF (C-4)."*  "blocked" implies certainty; WAFs mitigate, they do not guarantee blockage.

**Why it matters:** This thesis is an analytical design study. Its validation is expert review and attack-tree replay, not live penetration testing or deployment measurement. Using operational verbs creates a mismatch between the claims and the evidence, which an examiner will identify.

**How to fix it:** Apply a consistent verb replacement:

| Current verb | Evidence-bounded replacement |
|---|---|
| "is achieved through" | "is designed to be achieved through" / "the analysis indicates that security can be maintained by..." |
| "are neutralized by" | "are addressed by" / "the proposed controls are designed to reduce the feasibility and impact of" |
| "cannot be used on" | "is intended to prevent use on" / "the binding mechanism significantly raises the barrier to" |
| "are blocked by" | "are mitigated by" / "the WAF is configured to detect and block" |

Specifically for the RQ1 answer (Section 6.7), revise the opening:
> *"Security is achieved through a layered defense-in-depth architecture..."*
to:
> *"The analysis showed that a layered defense-in-depth architecture provides the strongest available basis for protecting ... Application-layer encryption with HMAC-based ..."*

---

### 3. Reduce overlap between Sections 5.5 (Chapter 5 limitations) and 6.5 (Chapter 6 limitations)

**What is wrong:** Both Chapter 5 (Section 5.5) and Chapter 6 (Section 6.5) contain limitations sections. The Chapter 5 limitations are methodological in nature (specific to the threat analysis and gap-analysis methodology). The Chapter 6 limitations partly repeat the same points at a higher level. Having two limitations sections with overlapping content makes the thesis read as repetitive.

**How to fix it:** Distinguish the two sections clearly:

- **Section 5.5 (Chapter 5)**: Methodological limitations: constraints specific to the threat analysis, the attack-tree construction, and the gap analysis methodology. Keep this section in Chapter 5.
- **Section 6.5 (Chapter 6)**: Thesis-level limitations: broader constraints on generalizability, scope, validation approach, and applicability. Remove from Chapter 6 any point that is already covered in the same words in Section 5.5.

---

### 4. Define the P×I numerical mapping in Chapter 5 before using it in Table 6.2

**What is wrong:** Table 6.2 uses a numerical P×I scale (scores of 4, 5, 8, 15, 25, etc.) to show pre- and post-control risk scores. The mapping from the qualitative High/Medium/Low/Critical labels in Chapter 5 to the numerical scores is not defined anywhere in the thesis.

**Why it matters:** Without the explicit mapping, Table 6.2 cannot be reproduced by another researcher. The numbers appear without derivation.

**How to fix it:** Add the mapping table to Section 5.2.1 in Chapter 5 (see also Chapter 5 feedback, Issue 3). Once that mapping is defined in Chapter 5, Table 6.2 will be correctly grounded.

---

### 5. Consider tightening the RQ answers in Section 6.7

**What is wrong:** The RQ answers in Section 6.7 are present and complete, but they are longer than necessary. RQ1, in particular, includes a full list of controls. A discussion-chapter RQ answer should state the answer directly and reference the evidence, not re-introduce the full solution.

**How to fix it:** Keep the structure (one paragraph per RQ) but shorten each answer to 3–4 sentences that state the conclusion and reference the evidence location. For example:

> *"RQ1 was answered by deriving cybersecurity requirements from application-layer encryption, mutual authentication.., each mapped to the specific threats and standards gaps identified in Chapter 5. The full control set is detailed in Section 5.5 (proposed framework)."*
