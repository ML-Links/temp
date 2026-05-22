# Abstract 


## Overall assessment

The abstract is well structured and covers the most important elements: the problem context, the methodology (STRIDE, attack trees, gap analysis, framework design), the scope of the analysis, and the main contribution. It is self contained and gives a reader a clear overview of the thesis.

However, there are a few structural issues and minor flow problems.

---

## What works well

- The problem is clearly framed: UAVs + 5G + cloud = a multi-domain attack surface that existing standards do not address.
- The methodology is named explicitly: STRIDE, attack trees, clause-level gap analysis, framework design.
- The main findings are present: threat counts, gap counts, framework layers, risk reduction.
- Keywords are included.
- The abstract is self-contained: a reader can understand the thesis without reading anything else.
- The contribution is clearly identified.

---

## Issues to address

### 1. Verify the university abstract format

University guidelines require a bibliographic header above the abstract text containing author names, thesis title, degree, supervisor etc.

---


### 2. Referencing an Appendix in the Abstract

*   **What is wrong:** An abstract must be a completely standalone document. *"identifies 80 distinct threats across eight system components (Appendix A)."* 

*   **THow to fix it:** Remove the reference to the appendix. 

>  "...identifies 80 distinct threats across eight system components."

---


### 3. Specific Commercial Models

*   **What is wrong:** Mentioning *"the DJI M350 RTK UAV, DJI Dock 3, FlightHub 2 on Microsoft Azure"* makes the research sound like a specific product evaluation rather than a generalizable scientific framework. While it's great to mention these in the thesis methodology, they clutter the abstract.

*   **How to fix it:** Broaden the terms to highlight the *class* of technology, using the brand names only as examples. 

>  "A reference architecture is constructed using enterprise-grade hardware and software—including an RTK-enabled UAV, an automated docking station, and a cloud fleet-management platform (e.g., DJI and Microsoft Azure)—connected via a public 5G network with an IPsec VPN."

---


### 4. Reduce density 

*   **What is wrong:** *"revealing 94 3GPP, 53 NIST, 10 ISO/IEC, and 9 CSA gaps."* Listing exact counts of gaps across four different standards breaks the reading flow and forces the reader to process too much granular data. 
*   **How to fix it:** Combine the numbers to focus on the *impact* and scale of your findings, rather than the exact itemized counts.

> "...revealing over 160 specific control gaps across the evaluated frameworks."

---

### 5. Jurisdictional ambiguity 

*   **What is wrong:** *"across three jurisdictions"* is slightly ambiguous. Does this mean three legal/geographic jurisdictions (e.g., US, EU, China) or three network domains (MNO, Internet, Cloud provider)? 

*   **ow to fix it:** Clarify the word "jurisdictions" to ensure the reader knows what type of boundary you are talking about.

> "...across three distinct administrative domains with no single security authority."

---

### 6. Soften verbs where the evidence is analytical, not empirical

**What is wrong:** The abstract uses "demonstrates" in the sentence: *"Quantified risk reduction demonstrates a 40% to 75% decrease in risk scores..."* The verb "demonstrates" implies an empirically measured outcome from a live or tested system. This thesis uses a qualitative Plausibility × Impact scoring model without live system testing or penetration testing.

**How to fix it:** Replace "demonstrates" with "indicates" or "shows," and add a short qualifier. For example:

> "The risk-scoring analysis indicated a 40% to 75% reduction ..."

---

### 7

> Please verify compliance with the full university abstract block, especially the bibliographic header and one-page limit.