# Chapter 5: Results and Analysis

## Overall assessment

Chapter 5 is the strongest chapter in the submission. The STRIDE rating methodology is now defined upfront in Tables 5.0.1 and 5.0.2. The attack trees include formal attacker model blocks (goal, capability, attack environment, success condition), making them reproducible and credible. The gap analysis is conducted at the clause level with specific standards references and a consolidated priority table. The limitations section (5.5) is present and appropriately bounded.

Only two issues remain. 

## Issues to address

### 1. Move the proposed cybersecurity framework into Chapter 5

**What is wrong:** Chapter 5 presents the threat analysis, attack trees, and gap analysis in detail. However, the *framework* (the directly designed output that responds to those findings) does not appear in Chapter 5. It is introduced in full only in Chapter 6 (Sections 6.2.1 through 6.2.5). This means the reader completes the entire results chapter without seeing the main contribution, then encounters it for the first time in the discussion chapter.

**Why it matters:** The results-and-analysis template expects the original contribution to appear in the results chapter. Chapter 6 should discuss, interpret, and evaluate a framework already introduced in Chapter 5. 

**How to fix it:** Add a final section to Chapter 5 (e.g., Section 5.5 and renumber 5.5 Limitations to 5.6) titled *"5.5 Proposed Layered Cybersecurity Framework."* This section should:

- State that the framework is derived from the STRIDE results, attack-tree scenarios, and gap analysis.
- Present the five-layer structure with the control identifiers.
- Include the risk-reduction table (currently Table 6.2) to show how the framework addresses the most critical threats.

Chapter 6 can then begin by referencing this framework and focus on interpretation, limitations, and answers to the research questions.

---

### 2. Fix the duplicate use of "Table 5.2"

**What is wrong:** The number "Table 5.2" is used for two different tables in Chapter 5:

- In Section 5.2.4: *"Table 5.2 — Security requirement comparison: C2 link vs. video and telemetry stream"*
- In Section 5.4.6: *"Table 5.2 — Consolidated critical gaps and priority"*

**How to fix it:** Renumber one of the two tables. The consolidated gap-priority table in Section 5.4.6 should become Table 5.6 (or the next available number). 

> Check all cross-references to these tables throughout Chapters 5, 6, and 7 and update them accordingly.

---

### 3. Define the P×I numerical mapping used in Chapter 6's risk table

**What is wrong:** Tables 5.0.1 and 5.0.2 define plausibility as High/Medium/Low and impact as Critical/High/Medium/Low. Chapter 6 (Table 6.2) then presents a P×I score on a 1–25 scale (e.g., UD1/ND1 = 25, NT1 = 15). The mapping between the qualitative labels and the numerical scores is never defined in the thesis.

**Why it matters:** Without the mapping, the scores in Table 6.2 are not reproducible. A reader cannot verify whether "High × Critical = 25" or what the numerical value for "Medium × High" is. This undermines the claim that risk reduction is "quantified."

**How to fix it:** Add a small mapping table to Section 5.2.1, immediately after Tables 5.0.1 and 5.0.2:

| Plausibility label | P score |
|---|---|
| High | 5 |
| Medium | 3 |
| Low | 1 |

| Impact label | I score |
|---|---|
| Critical | 5 |
| High | 4 |
| Medium | 3 |
| Low | 1 |

> "Pre-control and post-control risk scores are computed as R = P × I. The range is 1–25. Scores of 20–25 are classified as Critical, 12–19 as High, 6–11 as Medium, and 1–5 as Low."

This makes the quantification in Chapter 6 traceable back to the definitions in Chapter 5.

> I also mentioned this in the feedback for Chapter 2, issue #10, so please coordinate with Kamel regarding this matter.

---

### 4. Soften forward-reference language that previews framework controls

**What is wrong:** Some passages in Chapter 5 already name specific Chapter 6 controls as motivations, before the framework has been introduced:

- *"directly motivates the onboard jamming-detection and fail-safe-behavior controls R‑3 and R‑4 in the proposed framework"* (Section 5.4.2)
- *"forcing the design to rely on application-layer encryption and HMAC integrity (R1)"* (Section 5.4.5)

These forward references are less problematic in Chapter 5 than in Chapter 3, because Chapter 5 leads directly into the framework. However, if the framework is moved into Chapter 5 (per Issue 1 above), these forward references become internal references and are resolved automatically. If the framework stays in Chapter 6, these references should be softened to say "application-layer encryption" or "a compensating application-layer control" rather than citing a specific control identifier.

