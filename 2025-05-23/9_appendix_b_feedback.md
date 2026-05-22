# Appendix B: Clause-Level Standards Gap Mapping 

## Overall assessment

The structure follows the correct format for a clause-level gap analysis. The remaining issues are completeness verification, consistency with Chapter 5's claims, and the introductory note.

---

## What works well

- The table format is consistent with what Chapter 5 references.
- The visible entries are specific and accurate.
- The entries reviewed (B.1.1 for TS 22.125 with 6 gaps, B.1.2 for TS 33.125 with 5+ gaps, B.1.3 for TS 33.501 with 9 gaps) show the expected level of analytical depth for master-level work.
- The appendix is organized by framework and then by specification, which matches the structure described in Chapter 5.

---

## Issues to address

### 1. Ensure consistent terminology between Appendix B and Chapter 5

**What is wrong:** The threat IDs in the gap-mapping entries (e.g., N-T1, U-T1, A-S1) must match exactly the threat IDs used in Chapter 5 (Table 5.1) and Appendix A.

**How to fix it:** After deciding on a consistent threat ID format (see Appendix A feedback, Issue 3), apply the same format throughout Appendix B.

---

### 2. Consider adding a summary coverage table at the end of each framework section

There is currently no quick visual showing how many gaps exist per component, control family, or STRIDE category within each framework.

**How to fix it:** At the end of each major section (B.1, B.2, B.3, B.4), add a small summary table:

> | Control family / Standard section | Gap count |
> |---|---|
> | TS 22.125 | 6 |
> | TS 33.125 | 5 |
> | TS 33.501 | 9 |
> | ... | ... |
> | **Total 3GPP** | **94** |

This makes the appendix self-verifiable without requiring the reader to count rows.

---

### 3. Verify all claims

- Gap entries reference specific clauses (e.g., TS 22.125 §5.4.001, TS 33.501 §5.11, Annex D). Confirm that all clause numbers are accurate against the actual standards documents. 
- Count the total gap entries in the formatted Word document across all four framework sections. Confirm:
  - B.1: Total 3GPP entries = 94 across 13 subsections
  - B.2: Total NIST entries = 53
  - B.3: Total ISO/IEC entries = 10 (5 for 27017 + 5 for 27018)
  - B.4: Total CSA entries = 9



