# Chapter 2: Method and Material


## Overall impression

The five-step methodology workflow is logical and traceable, the Assumptions table is well structured and  useful, the Expert Review section is detailed enough to be credible, and the Division of Labour is specific and clear. The overall architecture of the chapter, from research design through methodology, validation, assumptions, and roles, is appropriate for this chapter.

Three things still need to be addressed. 

---

## Issues to address

### 1. Quantitative results still appear in the methodology chapter

Two result-style quantitative claims remain in Chapter 2:

1. Step 5 includes: "a layered cybersecurity framework is designed. The framework organizes over thirty specific controls"
2. Step 5 also includes: "demonstrating a 40% to 75% risk reduction and a shift in the system's overall security posture to an acceptable level."

These are findings, not methodology descriptions. A reader encountering "40 % to 80 % risk reduction" in Chapter 2 is reading the answer before the question has been posed.

**Why this matters:** Methodology chapters describe the process and the type of output expected, not the actual numerical findings. Mixing the two makes both the methodology and the results chapters harder to read, and it weakens the persuasiveness of the results when the reader reaches them.

**How to fix it:** In Step 5, describe the process and the type of output without giving the actual numbers. The specific results belong in Chapter 5 or 6. For example:

Instead of:
> "Pre- and post-control risk scores are compared for the eight most critical threats, demonstrating a 40% to 75% risk reduction.."

Write:
> "Pre- and post-control risk scores are compared for the five most critical threats in order to evaluate the relative effectiveness of the proposed controls. The results of that comparison are presented in Chapter 5."

Instead of:
> "The framework organizes over thirty specific controls..."

Write:
> "The framework organises a set of specific controls into four layers, each linked to the threat catalogue and gap analysis."

---

### 2. Reliability and Validity subsection is missing

Section 2.3 is titled "Validation Approach" and covers two useful mechanisms: scenario-based analysis and expert review, but it does not address reliability and validity as a research methodology concept. Specifically, it does not explain how the study can be reproduced by another researcher, how researcher bias is limited in the judgment-based steps, or how the validity of the qualitative analysis is established beyond the two named validation mechanisms.

**How to fix it:** Add a subsection titled "2.3.1 Reliability and Validity" or restructure Section 2.3 to include these elements alongside the existing content. The subsection should address:

- **Reliability**: the workflow is repeatable because steps are documented, the standards corpus is fixed and named, and the plausibility/impact rating criteria are predefined. Another researcher following the same five steps with the same architecture description and the same standards would produce comparable results.
- **Validity**: the analysis is grounded in real architecture (DJI M350 RTK, Microsoft Azure), real standards documents (named and versioned), and real attack tooling (USRP B210, srsRAN, SSLstrip). The expert review provides an external check on the completeness and plausibility of the threat catalogue.
- **Limitations**: acknowledge where judgment cannot be fully removed (e.g., the plausibility ratings involve estimation, not empirical measurement).

Example:

> "The method is considered reliable because it follows a structured five‑step process... Validity is strengthened in two ways.... The primary limitation is that the plausibility ratings rely on expert judgment rather than empirical probability measurements. As a result, the ratings should be interpreted as informed estimates rather than quantified values."


---

### 3. Several methodological claims still lack citations

The following claims in the body text are stated as established facts but have no citation marker:

1. **STRIDE introduced in Step 2:** STRIDE is named and described at length, but there is no citation for the method itself at its first mention. STRIDE should be cited when it is introduced.
2. **Attack Trees introduced in Step 3** — Same issue. The method is named and described without a citation at first mention.
3. **NIST SP 800-30 mentioned in Step 2:** The plausibility and impact rating scale is described as "adapted from NIST SP 800-30 and the ENISA UAV Threat Landscape." NIST SP 800-30 and the ENISA report are not cited at this point.
4. **Triangulation claim in 2.3:** The closing sentence of Section 2.3 describes "triangulation between academic rigour and industry pragmatism" as "accepted practice in qualitative cybersecurity research." This is a methodological claim that requires a citation.

**How to fix it:** Add citation markers at each of these points. Use the same sources cited in Chapter 4 for STRIDE [111] and Attack Trees [117, 118], add NIST SP 800-30 as a reference, and add a methodological reference for triangulation in qualitative research.

Example fix for Step 2:
> "The STRIDE methodology [X] is applied to each component and each data flow crossing a trust boundary. Each threat is rated on two qualitative dimensions using a scale adapted from NIST SP 800-30 [Y] and the ENISA UAV Threat Landscape [Z]."

---

### 4. ISO/IEC 27001 inconsistency between assumptions and standards used

The Assumptions table in Section 2.4 states: "The emergency response organisation maintains an information security management system aligned with ISO/IEC 27001." This is reasonable. However, the standards corpus for the gap analysis in Step 4 lists ISO/IEC 27017 and ISO/IEC 27018, not ISO/IEC 27001. A reader going from 2.4 to Step 4 may wonder whether 27001 is part of the analysis or only a background assumption.

**Example fix**: add one sentence in Step 4 that clarifies the role of each standard. For example:

> "ISO/IEC 27001 provides the governance framework assumed to be in place at the emergency response organisation (Table 2.1). The analytical standards for this gap analysis are ISO/IEC 27017 and ISO/IEC 27018, which extend the 27001 governance layer with cloud-specific controls .."

---

### 5. Good to Consider: Name the research methodology more precisely

The study is described as a "qualitative research design complemented by structured modeling
techniques" This is adequate, but the design can be named against a recognized research methodology taxonomy. The study closely resembles design science research (DSR), since it produces an artefact (the cybersecurity framework) through a systematic design process grounded in analysis. Alternatively, it could be framed as a case study methodology.

If you choose to be more specific, one sentence would be enough:

> "The study follows a design science research (DSR) methodology, in which a cybersecurity framework artefact is constructed through a structured, analytical process grounded in threat modelling and standards gap analysis [DSR reference]."

This would strengthen the methodological framing.

---

### 6. Describe the data collection process and materials more concretely

The current text explains what was analyzed, but it does not yet explain the collection process in enough detail for reproducibility.

**Why this matters**: Methodology chapters are stronger when they tell the reader exactly where the material came from, how it was selected, and what the researcher did with it.

**How to fix it:**

- State how literature was searched.
- Name the databases, standards portals, and other repositories used.
- Define inclusion and exclusion logic.
- State the time window for the literature review.
- List the exact standards corpus used in the gap analysis.
- Explain what outputs or artifacts were produced at each step.

**Example fix**:

> "The literature review covered sources published between 2020 and 2026 and focused on three domains: UAV cybersecurity, 5G security, and cloud security. Academic literature was identified through databases such as ???, while standards documents were collected from the official 3GPP, NIST, ISO/IEC ..."


---

### 7. Expert Review

1. **The newly submitted draft is missing the "Expert Review"** content previously included in Section 2.3. The earlier draft contained the following discussion:

> The complete threat catalogue, attack trees, gap analysis, and proposed framework were reviewed by domain experts from two communities:
> - Academic researchers in UAV security and 5G network security assessed the methodological rigour, the completeness of the threat modelling, and the alignment of the findings with current research literature.
> - Industry practitioners with direct experience in Azure cloud security architecture and telecommunications security evaluated the practical feasibility of the attack scenarios, the correctness of the cloud‑specific configurations, and the implementability of the proposed controls within typical enterprise constraints. Feedback from expert review was incorporated to refine threat descriptions, adjust plausibility and impact ratings, and ensure that the framework’s controls are expressed at a level of detail suitable for engineering teams. This dual‑review process aligns with accepted practice in qualitative cybersecurity research, where triangulation [Ref_here] between academic rigour and industry pragmatism strengthens the validity of the findings.

2. **The expert-review is too brief.**

**Why this matters**: If expert review is used to support validity, the reader needs enough detail to understand who was involved, what was reviewed, and how that feedback influenced the study.

**How to fix it:**

- State how many experts participated.
- Briefly describe their qualifications.
- Explain how they were selected.
- State what material they reviewed.
- Explain how their feedback was incorporated.

**Example fix**:

> "Expert review involved two groups: academic researchers with experience in UAV and 5G security, and industry practitioners with experience in Azure cloud security and telecommunications security. Reviewers were given the threat catalogue, selected Attack Trees, and the draft standards-mapping tables. Their feedback was used to ..."


---

### 8. Resolve the research-design wording so it matches the method actually used

The chapter introduces the study as qualitative, but later describes numerical risk scoring and percentage-
based risk reduction.

**Why this matters**: This creates a small but important inconsistency. The reader should understand whether the study is purely qualitative or qualitative with a semi-quantitative scoring component.

**How to fix it**:

- Either describe the study as a qualitative design with a semi-quantitative risk-scoring component, or
keep it fully qualitative in Chapter 2 and move the numerical outcomes entirely to the results chapter.

**Example fix**:

> "The study follows a qualitative research design supported by semi-quantitative risk scoring ... The scoring model is used to structure prioritization, not as a statistical validation method."

---

### 9. Strengthen the Assumptions subsection

Section 2.4 is too brief.

**How to fix it**:
- Expand the subsection into a paragraph set.
- State the major analytical assumptions clearly.

**Example fix**:

> "This study assumes a reference architecture built around a DJI M350 RTK platform, public 5G connectivity, and an Azure-hosted command-and-control backend. No live hardware deployment or firmware modification is performed. The analysis is ..."¨

---

### 10. Mathematical/Methodological mismatch in the Risk Matrix

Section 2.2, Step 2 defines the qualitative scales with **three** levels for Plausibility (*High, Medium, Low*) and **four** levels for Impact (*Critical, High, Medium, Low*). However, Step 5 notes that the risk is quantified using a **5 × 5 Plausibility × Impact matrix**. Because a 5x5 matrix requires five distinct levels for each dimension, the scales defined in Step 2 currently do not align with the matrix in Step 5.


**How to fix it:* expand the definitions in Step 2 so they perfectly match the 5x5 grid.

**Example fix:** update Step 2 to include five levels for each metric:

> *   **Plausibility:** *Very High* (automated tools available, no skill required), *High* (achievable with commercial, widely available tools and limited expertise), *Medium* (requires specialised knowledge or equipment but published proof-of-concept exists), *Low* (requires nation-state capability or insider access, no known public exploit), *Very Low* (theoretical only).
>
> *   **Impact:** *Critical* (complete mission failure, loss of UAV, or exfiltration of all sensitive data), *High* (major mission degradation...), *Medium* (partial degradation...), *Low* (minor inconvenience...), *Very Low* (negligible effect).


> I also mentioned this in the feedback for Chapter 5, issue #3, so please coordinate with Sharaf regarding this matter.

---

### 11. Sudden introduction of "AI/LLM In Section 2.2, Step 5

If AI/LLM is outside the primary scope, you can remove it from Step 5.


