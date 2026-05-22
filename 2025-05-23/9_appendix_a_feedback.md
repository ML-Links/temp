# Appendix A: Complete STRIDE Threat Catalogue (80 Threats) 

## Overall assessment

The structure is correct and the entries visible in the review follow the format expected for a supporting appendix: threat ID, STRIDE category, description, plausibility, impact, and associated data flows. 

The remaining issues are about completeness verification, cross-reference accuracy, and the introductory note.

---

## What works well

- The threat table format is clear and consistently structured across the components visible in the reviewed text.
- Threat IDs follow a logical naming convention (component prefix + STRIDE category initial + number).
- Plausibility and impact ratings are included and the entries reviewed are consistent with the definitions in Chapter 5 (Tables 5.0.1 and 5.0.2).
- Data flow references are included (e.g., DF1, DF2, DF8), which enables cross-referencing with Chapter 3's Table 3.2.
- The appendix covers multiple components (UAV, Dock 3 ...).

---

## Issues to address


### 1. Strengthen the introductory paragraph

**What is wrong:** The submitted appendix has a short introductory note. The note should explicitly state how the appendix is organized, what each column means, and how the entries relate to Chapter 5.

**Why it matters:** A reader jumping directly to the appendix to trace a specific threat ID should be able to understand the structure without reading Chapter 5 first.

**How to fix it:** Expand the introduction to include:

> *"This appendix presents the complete STRIDE threat catalogue used in Chapter 5. Threats are organized by system component. Each entry includes a unique threat ID, the STRIDE category...."*

---

### 2. Confirm ID and terminology consistency with Chapter 5

**What is wrong:** Chapter 5 uses threat IDs such as "U-S1," "U-D1," and "N-T1" in the text and tables. The appendix uses "US1". Confirm that the formatting in the Word document uses a consistent notation throughout Appendix A and matches exactly what Chapter 5 uses.

**Why it matters:** If Chapter 5 references "U-S1" and Appendix A shows "US1", cross-referencing becomes ambiguous.

**How to fix it:** Choose one notation style for threat IDs (e.g., U-S1) and apply it consistently in Chapter 5, Table 5.1, and Appendix A.

---

### 3. Consider adding a one-line summary row per component showing the threat count

**What is wrong:** There is no quick way for a reader to verify the distribution of 80 threats across 8 components without counting rows.

**How to fix it:** Add a header row or a short summary line at the start of each component section, for example:

> *"DJI M350 RTK UAV:10 threats (U-S1 to U-E1)"*
> *"DJI Dock 3 (with 5G Router): [n] threats (D-S1 to D-E[n])"*

This makes the appendix much easier to navigate and allows quick verification of the total count.

> Also Verify all 80 threats are present and count is accurate




