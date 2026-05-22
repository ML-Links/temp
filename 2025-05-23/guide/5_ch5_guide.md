# Guide: Chapter 5 - Results and Analysis

## What this guide does

This guide explains Chapter 5 in simple words. It walks through the actual findings of the thesis: the threat catalog, the attack scenarios, and the standards gaps.

## Chapter 5 in one simple view

- This is the main evidence chapter of the thesis.
- The student presents three big analytical outputs.
- First, a STRIDE threat analysis across the system.
- Second, two attack trees showing how major attacks could unfold.
- Third, a standards gap analysis showing where 3GPP, NIST, ISO/IEC, and CSA material fail to cover the identified threats.
- The chapter is trying to prove that the UAV-5G-cloud system has a real multi-layer threat landscape and that current standards do not close it fully.

## How to read this chapter

- Read it as the proof chapter.
- The student is no longer just describing the system or the theory.
- The student is now showing what the actual analysis produced.
- Keep track of the relationship between Chapter 3 architecture, Appendix A threats, Appendix B clause mapping, and the claims made here.

## Detailed reading guide

### 5.1 Introduction

#### What this section says in simple words

- The student begins by reminding the reader of the thesis system: DJI drone, Dock, browser, FlightHub 2 on Azure, and public 5G.
- The section says this setup enables BVLOS operation but also creates a broad attack surface.
- Then the student clearly names the three analytical workstreams in the chapter.
- These are STRIDE threat modeling, attack tree modeling, and consolidated standards gap analysis.
- The section also says the chapter addresses the research question about where standards fall short.
- The student emphasizes that the findings are tied to the trust boundaries and data flows defined in Chapter 3.

#### What the reader should understand from this section

- Chapter 5 is the analytical center of the thesis.
- Everything here is supposed to be evidence-based and traceable to earlier structure.
- The student is now moving from setup to findings.

### 5.2 STRIDE Threat Analysis

#### What this section says in simple words

- This part presents the threat catalog produced through STRIDE.
- The student is showing what kinds of threats exist across the eight system components.
- The point is not only to list threats, but also to rate and prioritize them.

### 5.2.1 Scope and Rating Methodology

#### What this subsection says in simple words

- The student says STRIDE was applied to eight components.
- These include the UAV, Dock, browser, FlightHub 2, public 5G network, Azure Front Door, Azure VPN Gateway, and Azure Communication Services.
- Each threat is rated on plausibility and impact.
- Plausibility tells how easy or realistic the attack is.
- Impact tells how badly the system or mission would suffer if it succeeds.
- The student defines three levels for plausibility and four for impact.
- This rating method creates the basis for selecting the most serious threats.

#### What the reader should understand from this subsection

- This is the scoring logic behind the chapter.
- Without this part, later claims about high-risk threats would have no method.

### 5.2.2 Critical Threats Per Component

#### What this subsection says in simple words

- The student then presents the most critical threats for each major component.
- For the UAV and network side, rogue gNB impersonation, RF jamming, and command tampering are among the most severe.
- For the Dock side, certificate theft and default credentials appear as major problems.
- For the browser side, JWT theft and phishing are key concerns.
- For FlightHub 2, SQL injection or container escape are highlighted.
- For the cloud-facing services, DDoS, certificate misuse, management compromise, and room or token abuse are included.
- The student is using this table to show that the system has critical exposures across radio, browser, cloud, and service layers.

#### What the reader should understand from this subsection

- The risk is distributed across the entire chain.
- No single layer is the only problem.
- Spoofing and denial-of-service especially stand out among the most severe threats.

### 5.2.3 Discussion of the Threat Landscape

#### What this subsection says in simple words

- Here the student interprets the threat catalog instead of only listing it.
- The student says spoofing and denial-of-service dominate the threat landscape.
- The UAV and the 5G radio side are especially exposed because they sit on the outer edge of the system and can be attacked physically or over the air.
- The chapter also points out that cloud and browser weaknesses can become catastrophic because they can affect command authority.
- The missing user-plane integrity in 5G is given strong attention because it can enable tampering even in an otherwise standards-compliant network.

#### What the reader should understand from this subsection

- The thesis is building the argument that cross-layer security is necessary.
- Radio threats, browser threats, and cloud threats all matter.
- The system cannot be protected by focusing on only one domain.

### 5.2.4 Comparative Security Requirements for C2, Video, and Telemetry

#### What this subsection says in simple words

- The student explains that not all data streams need the same protections.
- C2 traffic needs the strongest integrity and availability because wrong commands can cause physical harm.
- Video needs confidentiality and enough performance for live awareness, but it is somewhat more tolerant of delay or corruption than command traffic.
- Telemetry also matters strongly because false telemetry can mislead the operator.
- The student uses this comparison to justify why the architecture separates C2 and telemetry from video handling.
- In simple terms, the chapter is saying that security design must reflect the different roles of different streams.

#### What the reader should understand from this subsection

- This is one of the places where the thesis directly addresses how to secure command, telemetry, and video differently.
- It supports later design choices around messaging paths and protection mechanisms.

### 5.3 Attack Tree Modeling

#### What this section says in simple words

- After the broad threat map, the student zooms in on two detailed attack scenarios.
- The purpose is to show step-by-step attacker logic.
- Instead of only saying a threat exists, the student shows how an attacker could actually move through the system.

### 5.3.1 Scenario 1: Forced Landing via Rogue gNB

#### What this subsection says in simple words

- In this scenario, the attacker wants to force the UAV to land at a chosen location.
- The attacker uses a rogue base station built with software-defined radio equipment and open-source 5G software.
- The scenario assumes no insider access is needed.
- The attack tree shows four broad stages.
- First, establish the rogue gNB or overpower the legitimate signal.
- Second, make the UAV attach to it.
- Third, weaken or disable encryption or integrity protections.
- Fourth, inject the landing command.
- The student connects this attack directly to weaknesses around optional ciphering and user-plane integrity in 3GPP.

#### What the reader should understand from this subsection

- This is the thesis's most radio-centric critical scenario.
- The attack is important because it turns standards-level weakness into a concrete mission-safety consequence.
- It supports the argument that network compliance alone may still leave a dangerous gap.

### 5.3.2 Scenario 2: Unauthorized Flight Commands via Stolen JWT

#### What this subsection says in simple words

- In this scenario, the attacker wants to issue unauthorized commands by stealing the operator's JWT.
- The attacker may obtain the token through malware, phishing, or network-based interception conditions.
- Once the token is stolen, the attacker can replay it to FlightHub 2 or to the MQTT path if binding and lifetime protections are weak.
- The tree then ends with the attacker sending a malicious command such as a waypoint change or return-to-home action.
- The student uses this scenario to show that cloud and browser-side identity weakness can become flight-control weakness.

#### What the reader should understand from this subsection

- This is the thesis's main application-layer critical scenario.
- It proves that command compromise does not require attacking the radio side if the token and web side are weak.

### 5.4 Gap Analysis of Security Standards

#### What this section says in simple words

- This section compares the identified threats against major standards families.
- The student is asking a direct question: do current standards actually cover the problems revealed by the threat analysis and attack trees?
- The answer developed by the chapter is no, not fully.

### 5.4.1 Methodology

#### What this subsection says in simple words

- The student explains that mandatory requirements from the selected frameworks were gathered and classified.
- Each relevant requirement was judged as Met, Partial, or Gap.
- The student then mapped the gaps back to the threats and attack-tree elements.
- In simple terms, the chapter is trying to make the standards analysis systematic rather than impressionistic.

### 5.4.2 3GPP Specifications

#### What this subsection says in simple words

- This is the most directly network-related standards discussion.
- The student says the 3GPP review found many gaps for safety-critical aerial IoT use.
- The section highlights issues such as null cipher and integrity negotiation, missing user-plane integrity for C2, and other shortcomings in how public 5G standards handle the UAV problem.
- The student is using this subsection to argue that mobile standards help, but do not completely solve secure UAV command and control.

### 5.4.3 NIST SP 800-53 Rev. 5

#### What this subsection says in simple words

- Here the student evaluates how a general enterprise-style control framework fits the UAV-5G-cloud case.
- NIST provides broad control language, but it is not written specifically for aerial IoT over public mobile infrastructure.
- The implication is that useful control ideas exist, but some UAV-specific or infrastructure-sharing problems remain uncovered or under-specified.

### 5.4.4 ISO/IEC 27017 and 27018

#### What this subsection says in simple words

- This subsection focuses on cloud responsibility and privacy.
- ISO/IEC 27017 helps structure cloud-security responsibility thinking.
- ISO/IEC 27018 helps think about privacy and personal data handling in public-cloud environments.
- The student uses these standards to show where the Azure-hosted UAV system is supported and where cloud-specific or privacy-specific gaps remain.

### 5.4.5 CSA Cloud Controls Matrix v4.1

#### What this subsection says in simple words

- The student uses CSA CCM to evaluate cloud-native control coverage.
- This matters because the thesis system is not just a UAV platform; it is also a cloud-hosted command-and-control environment.
- The student suggests that even this cloud-focused framework does not fully address all edge-device, MQTT, streaming, and operational-technology concerns in the thesis case.

### 5.4.6 Recurring Thematic Gaps and Consolidated Priorities

#### What this subsection says in simple words

- This is the synthesis point of the standards analysis.
- Instead of keeping the gaps separated by framework, the student groups them into recurring themes.
- These themes include weak treatment of physical and radio-layer threats, poor coverage of edge-device responsibility, inadequate protection for real-time streaming and control data, immature AI or LLM security treatment, insufficient privacy controls for UAV payload data, and unmanaged multi-tier supply-chain risk.
- In simple words, this subsection turns many clause-level gaps into a smaller set of strategic weaknesses.

#### What the reader should understand from Section 5.4

- The thesis is not claiming that standards are useless.
- It is claiming that they are partial and fragmented.
- Together they still leave important end-to-end gaps in the UAV-5G-cloud problem.

### 5.5 Limitations

#### What this section says in simple words

- The student ends the chapter by acknowledging that the analysis has limits.
- The results depend on the chosen case architecture, the chosen frameworks, and documentary rather than live operational validation.
- In simple words, the student is saying the findings are structured and useful, but they are still bounded by the scope of the thesis.

## Quick recap of Chapter 5

- Chapter 5 presents the thesis evidence.
- It identifies major threats across the UAV-5G-cloud architecture.
- It then shows two detailed attack scenarios: rogue gNB forced landing and stolen JWT command injection.
- After that, it compares the threat landscape against 3GPP, NIST, ISO/IEC, and CSA standards.
- The chapter's main conclusion is that the system has real cross-layer risks and that current standards leave recurring gaps.
- If Chapter 5 is read correctly, the reader should finish it convinced that the thesis problem is concrete, evidence-backed, and not fully solved by existing standards.