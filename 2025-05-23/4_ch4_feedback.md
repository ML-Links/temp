# Chapter 4: Theoretical Background


## Overall assessment

Chapter 4 is much broader and better structured than the earlier draft. The chapter now contains the new Sections 4.1 and 4.2, which significantly expand the scope of the discussion. That expansion can work, but only if those sections are kept tightly connected to the thesis problem and do not start duplicating Chapter 3.

---

## What works well

- The chapter has a clear high-level structure from contextual theory to security concepts, standards, methods, and AI-related concepts.
- The 4.3 to 4.6 sequence is logical and broadly appropriate for a master-level theoretical background.
- The standards overview and the STRIDE plus attack-tree discussion are in the right chapter conceptually.
- The chapter shows much better breadth than a narrow literature summary.

---

## Issues to address

### 1. Tighten the newly added Sections 4.1 and 4.2 so they support the thesis directly

The current draft now includes two major new sections:

- 4.1 UAV Use Cases in Smart Cities
- 4.2 Smart City ICT Infrastructure

> Keep only the material that directly supports the emergency-response UAV problem, the later threat analysis, and the standards gap analysis. Trim any subsection that functions only as general smart-city background.

---

### 2. Correct the figure numbering in Section 4.2

Section 4.2 refers to the figure as Figure 3.1, and the caption also shows Figure 3.1, even though the figure appears inside Chapter 4.

**How to fix it:** Renumber the figure according to the Chapter 4 sequence and update all references to it accordingly.

---

### 3. Resolve the ISO and standards-version inconsistencies

This chapter contains two related consistency problems.

1. The ISO/IEC 27001 governance relationship is still unclear.
2. The version of ISO/IEC 27018 is inconsistent across the thesis.

In Chapter 2 and Chapter 5, the thesis refers to ISO/IEC 27018:2025, but Section 4.5.2 currently refers to ISO/IEC 27018:2019.

**Why this matters:** Standards-version consistency is essential.

**How to fix it:**

- Clarify the ISO/IEC 27001 governance-assumption role versus the analytical role of ISO/IEC 27017 and 27018.
- Use one exact version of ISO/IEC 27018 across Chapters 2, 4, 5, Appendix B, and the references.

---

### 4. Remove solution-forward and evaluative language from the theory chapter

Some passages in Chapter 4 do not remain neutral theoretical grounding. For example, Section 4.4.2 ends by saying that the 5G network and cloud-hosted C2 platform can serve as compensating controls and that this principle guides the framework design in Chapter 6.

**Why this matters:** Chapter 4 should explain theory, prior knowledge, and conceptual background. It should not start sounding like the thesis is already defending its own framework.

**How to fix it:** Rewrite these passages neutrally. Theoretical sections may explain why certain concepts matter, but they should not preview the thesis's solution as if it has already been established.

---

### 5. Increase critical synthesis, especially in Sections 4.1, 4.2, and 4.5

At the moment, too much of the chapter still reads as descriptive reporting. This is especially visible in the use-case survey and the smart-city ICT layer description.

**Why this matters:** The theoretical background should not only summarize source material. It should compare, evaluate, and identify what existing work does not yet solve for this thesis problem.

**How to fix it:** Add short synthesis statements at the end of major sections e.g.

- what these use cases have in common from a security perspective
- why the smart-city ICT model matters specifically for UAV security analysis
- why the four standards families are complementary rather than interchangeable

---

### 6. Explain why these frameworks and methods are used together

The chapter introduces UAV use cases, ICT layers, security concepts, standards, STRIDE, attack trees, and AI anomaly detection, but it still does not fully explain why this exact combination is the right theoretical foundation for the thesis.

**Why this matters:** This chapter should help the reader understand not only what the relevant theory is, but why these concepts were selected and how they fit together.

**How to fix it:** Add one short synthesis paragraph at the end of Section 4.5 or 4.6 explaining that:

- 3GPP covers the public 5G side
- NIST provides general control coverage
- ISO/IEC and CSA cover the cloud-responsibility side
- STRIDE and attack trees provide the analytical method for converting the architecture into threats and scenarios

---

### 7. Keep the AI anomaly-detection section clearly conceptual and secondary

Section 4.7 can stay, but it should remain clearly conceptual and future-oriented. At present it risks feeling like a hidden design subsection rather than theoretical background.

**Why this matters:** Since the thesis does not build, train, or test an anomaly-detection system, the theory chapter should not make AI or LLM material look like a core implemented result.

**How to fix it:** Keep the section short, explicitly mark it as complementary, and ensure it does not overshadow the main threat-modeling and standards-analysis logic.

---

### 8. Audit the references in this chapter carefully

This chapter is heavily reference-dependent, and it is one of the places where bibliography defects become visible fastest.

**What to check:**

- all standards documents cited here must exist in the reference list
- the versions must match the versions used later in Chapter 5 and Appendix B
- the citation style must match the rest of the thesis
- missing bibliography numbering gaps must be resolved, especially around the 140 to 169 range used in this chapter

> The reference list feedback should be applied here very carefully.