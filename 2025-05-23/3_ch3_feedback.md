# Chapter 3: Current State Analysis

## Overall assessment

This chapter has improved in several important ways. The ten-phase communication lifecycle is detailed and technically coherent, the Dock's role as the central communication hub is consistently described, the seven trust boundaries (A–G) are well defined and tabulated, and the ten primary data flows (DF1–DF10) are systematically catalogued. 

The remaining work is mainly about sharpening the chapter so it fully matches the purpose of *"Current State Analysis*. 

---

## Issues to address

### 1. Must Fix: Remove or replace all forward references to specific framework controls

**What is wrong:** The chapter repeatedly references specific control identifiers that belong to the Chapter 6 framework. Examples found in the submitted text:

- *"directly translates to the radio-layer compensations R-1 through R-5 in the proposed framework"* 
- *"motivates the application-layer encryption control R-1 in Chapter 6"*
- *"..loss of the MQTT connection would sever real-time control; this directly motivates the
deterministic failsafe behavior (R-4) and the MQTT hardening measures (C-6) in Chapter 6"*
- *"underscoring the importance of the container hardening control C10 in Chapter 6"* 
- *"This directly translates to the radio-layer compensations R-1 through R-5 in the proposed framework"* 
- *"underpins the cloud-layer controls (C-1 through C-10) developed in Section 6.2.3"*

**Why it matters:** Chapter 3 is the current-state analysis. Its role is to describe the system and identify its exposure points. The framework controls are the contribution of Chapter 5 (and currently, Chapter 6). Forward-referencing control codes from within Chapter 3 collapses the logical sequence of the thesis: the reader has not yet seen the analysis that justifies those controls, so the references are meaningless or misleading. It also reveals the thesis's solution before the problem has been fully characterized.

**How to fix it:** For every sentence that names a specific control code or references Chapter 6's framework, replace it with a forward-pointing observation about the *problem*, not the *solution*. Consistent replacement pattern:

> Instead of: *"directly translates to the radio-layer compensations R-1 through R-5 in the proposed framework."*
>
> Write: *"This boundary is exposed to radio-frequency threats including jamming and rogue base-station attacks, which are analyzed in Chapter 5."*

> Instead of: *"motivates the application-layer encryption control R-1 in Chapter 6."*
>
> Write: *"The MQTT control path is a critical channel in the security analysis that follows."*

Apply this correction to **every** instance where a control identifier (R-1 through R-5, C-1 through C-10, E-1 through E-7) appears in Chapter 3.

---

### 2. Must Fix: Add a closing synthesis section

**What is wrong:** The chapter ends abruptly after the data flows table (Table 3.2) and a short paragraph noting that "all data flows are either tunneled (IPsec) or protected by TLS." There is no section that synthesizes the current-state findings and states why they motivate the approach in Chapter 5.

**Why it matters:** The template for a Current State Analysis requires a closing subsection that identifies what the description revealed: the exposure areas, dependencies, and architectural characteristics that justify the analytical choices in the next chapter.

**How to fix it:** Add a closing subsection, for example Section 3.6, titled "Summary and Implications for the Security Analysis":

> *"The current-state analysis identified four security-relevant characteristics of the emergency UAV response architecture. First, the system spans three distinct trust domains ... Second, the architecture combines proprietary DJI protocols (DPP) with standard protocols ... Third, all UAV connectivity is mediated by the DJI Dock 3 ... Fourth, the Elsight DroneCommX 5G module's compatibility with the Dock 3 is treated as an operational assumption, since manufacturer confirmation was not available at the time of writing.*
>
> *These characteristics define the scope and structure of the threat modeling and standards-gap analysis in Chapter 5..."*

---

### 3. Should Fix: Remove remaining design-oriented commentary from Section 3.4.3

**What is wrong:** Section 3.4.3 ends with: *"The architecture enforces multiple layers of security: ... This layered approach minimizes exposure, enforces least privilege, and maintains end-to-end confidentiality."*

The phrase "this layered approach minimizes exposure and enforces least privilege" is a security evaluation claim, not a current-state description.

**Why it matters:** Chapter 3's role is to describe the system as it exists, (including the security mechanisms that are present) and to identify its exposure points. Concluding that the architecture "minimizes exposure" is the role of Chapter 6 (where the controls are evaluated). Chapter 3 should say what the security mechanisms *are*, not how effective they are.

**How to fix it:** Replace the evaluative conclusion with a neutral summary:

> *"The architecture incorporates multiple security mechanisms at each layer: .... The adequacy of these mechanisms for the identified threat landscape is analyzed in Chapter 5."*

---

### 4. Should Fix: Architectural assumptions in one location

**What is wrong:** The chapter mentions several assumptions in passing: the Elsight Dock 3 compatibility assumption is clearly stated in Section 3.4.1, which is good (*The DroneCommX 5G module compatibility with the DJI Dock 3 in this study will be assumed*). 

However, other assumptions are embedded in the description without being labeled as assumptions: for example, the assumption that the VPN tunnel uses mutual X.509 certificate authentication, and the assumption that the emergency response organization has a dedicated 5G network slice.

**Why it matters:** Explicitly labeled assumptions increase the chapter's analytical credibility.

**How to fix it:** Consider adding a short subsection (or table) in Section 3.5.3 titled "Architectural Assumptions," listing 3–5 key assumptions with a brief rationale and any source for each.

---


### 5. Section numbering gap

**What is wrong:** The chapter begins with Section 3.1 (Introduction) and then jumps to Section 3.4 (DJI UAV System). Sections 3.2 and 3.3 are missing from the submitted text.

---

### 6. Consider


Chapter 3 is the current-state analysis of the specific system under study. Its references should confirm facts about the system: vendor documentation, protocol specifications for protocols actually used, Azure service documentation, and deployment standards. Using Chapter 3 to carry general theoretical background blurs the boundary between the two chapters and weakens the analytical discipline of both.

Apply the following filter to every reference in Chapter 3: 

- ask "does this reference support a specific fact about the DJI/Dock/FlightHub/Azure system?" If yes, it belongs in Chapter 3. 
- If it instead supports a general concept (e.g., what STRIDE is, what zero-trust means in general, what 5G security architecture looks like in theory), move it to the relevant subsection of Chapter 4. 
- The rule of thumb: Chapter 3 references should be vendor documentation, RFCs, and deployment-specific technical documents; Chapter 4 references should be academic literature, standards frameworks, and theoretical models.
