# Guide: Chapter 2 - Method and Material

## What this guide does

This guide explains Chapter 2 in simple words. It retells the method chapter as a readable companion, so you can follow what the student actually did, in order, without constantly going back to the thesis text.

## Chapter 2 in one simple view

- This chapter explains how the thesis was carried out.
- The student says the work is qualitative and model-driven.
- The chapter builds a chain from system description to threat identification to attack decomposition to standards checking to framework design.
- In simple terms, the student is saying: first define the system clearly, then find the threats, then study the most important attack paths, then compare them against standards, then design controls.
- The chapter tries to show that the work is structured, traceable, and repeatable.

## How to read this chapter

- Read it as the method engine of the thesis.
- Check whether every later chapter really follows this workflow.
- Check whether the student explains not only what was done, but why that method makes sense for this problem.
- Check whether the chapter stays on process and does not start reporting results too early.

## Detailed reading guide

### 2.1 Research Design

#### What this section says in simple words

- The student says the thesis uses a qualitative research design.
- This means the work is not based on statistical experiments or large datasets.
- Instead, it is based on structured analysis of a complex technical system.
- The student argues that this is suitable because the topic is a multi-layer cyber-physical system involving drones, 5G, edge devices, and cloud services.
- The section then breaks the research design into four connected phases.
- The first phase is descriptive.
- In that phase, the student documents the architecture, components, protocols, data flows, and trust boundaries.
- The second phase is analytical.
- In that phase, STRIDE is applied to identify and rate threats.
- The third phase is decomposition.
- In that phase, the most critical attacks are broken into smaller attacker actions using attack trees.
- The fourth phase is evaluative and constructive.
- In that phase, the system is checked against standards, gaps are identified, and then a security framework is designed.
- The section ends by stressing traceability.
- The student wants the reader to believe that each control in the final framework can be traced back to a concrete threat and a concrete architectural weakness.

#### What the reader should understand from this section

- The thesis is not doing random security discussion.
- It follows a pipeline.
- The student wants the method to look disciplined and defensible.
- The key promise here is that the later framework will not be invented out of nowhere.
- It is supposed to come directly from earlier analysis.

#### Main ideas to keep in mind while reading

- Qualitative, not statistical.
- Structured, not impressionistic.
- Multi-phase, not one-step.
- Traceability is one of the main claims of methodological quality.

### 2.2 Methodology Overview

#### What this section says in simple words

- This section converts the broad research design into five practical steps.
- The student is now explaining the actual work process used in the thesis.
- Each step is meant to produce an output that becomes the input for the next step.

#### Step 1 - Literature Review and Architectural Documentation

##### What this step says in simple words

- The student first reviews literature and technical sources across three areas: UAV cybersecurity, 5G security, and cloud security or standards.
- This step is not only about collecting background reading.
- It is also used to build the reference architecture analyzed later in the thesis.
- The output is a concrete system model: the DJI M350 RTK, its payload, a 5G module, the Dock, the browser-based operator, FlightHub 2 on Azure, and the public 5G network.
- The student also says this architecture is broken into components, trust boundaries, and data flows.
- This is important because later threats are mapped to those exact elements.

##### What the reader should understand from this step

- The literature review is being used to construct the case system.
- The method starts by deciding what exact system is being studied.
- This makes the threat model more concrete.

#### Step 2 - STRIDE Threat Identification

##### What this step says in simple words

- The student then applies STRIDE to each component and to each data flow crossing a trust boundary.
- For every threat, the student records what is being targeted, how the attack could happen, and what mission effect it could cause.
- The student also defines two ratings: plausibility and impact.
- Plausibility measures how achievable the attack is.
- Impact measures how severe the effect would be if the attack succeeds.
- The chapter says this produces a full threat catalog, summarized in the thesis and fully listed in Appendix A.

##### What the reader should understand from this step

- This is the main threat-discovery step.
- The thesis is trying to show that threats were identified systematically, not chosen selectively.
- The rating system is the bridge to later prioritization.

#### Step 3 - Attack Tree Construction

##### What this step says in simple words

- After identifying many threats, the student chooses two critical scenarios for deeper analysis.
- These scenarios are considered high in both plausibility and impact.
- The student uses attack trees to break each scenario into smaller steps.
- AND logic means several conditions must all happen.
- OR logic means the attacker can choose between alternative ways to proceed.
- The section also says the leaf nodes are justified by literature or by available tools.
- So the student is trying to show that these attacks are not imaginary.

##### What the reader should understand from this step

- STRIDE gives the broad map of threats.
- Attack trees then zoom into the most serious paths.
- This step is about showing how an attacker can move through the system in practice.

#### Step 4 - Clause-Level Gap Analysis Against Standards

##### What this step says in simple words

- Once the threats are identified, the student compares them against four major standards families.
- These are 3GPP, NIST SP 800-53 Rev. 5, ISO/IEC 27017 and 27018, and CSA CCM.
- The student says the analysis follows four sub-steps: extract relevant requirements, group them by domain, assess how the system aligns with them, and prioritize the gaps.
- Each requirement is classified as Met, Partial, or Gap.
- The student then maps these gaps back to threats and attack-tree nodes.
- The chapter also gives the overall idea that many gaps exist across all four standards families.

##### What the reader should understand from this step

- The thesis does not stop at threat identification.
- It also asks whether current standards are enough.
- This is where the thesis builds its claim that existing governance is fragmented and incomplete.

#### Step 5 - Framework Design and Risk Reduction Quantification

##### What this step says in simple words

- The student then groups the identified gaps into recurring themes.
- These themes become the basis for the final security framework.
- The framework is organized into layers such as 5G network, edge device, cloud platform, AI or LLM, and organizational or privacy.
- Each control is meant to state what it does, how it is implemented, what threat it addresses, and what residual risk remains.
- The last part of this step is risk reduction.
- The student says the framework is evaluated using a plausibility-times-impact matrix.
- Pre-control and post-control scores are compared for the most critical threats.

##### What the reader should understand from this step

- The framework is supposed to come from the gap analysis, not from general best practice alone.
- The student also wants to show that the framework changes the overall risk posture in a measurable way.

#### What the reader should understand from the full methodology section

- The five steps form one chain.
- Literature gives the architecture.
- The architecture gives the threat model.
- The threat model gives the attack trees and the standards comparison.
- The standards comparison gives the framework.
- The framework gives the risk reduction discussion.

### 2.3 Validation Approach

#### What this section says in simple words

- This section explains how the student tries to make the findings credible.
- The main idea is not laboratory testing.
- The validation here is analytical and literature-supported.
- The attack trees are checked for logical consistency.
- Each leaf action is linked to published work, public exploit code, or known commercial hardware and software.
- The student also argues that the use of a real commercial UAV platform and a real cloud provider makes the scenarios representative rather than fictional.
- In simple terms, the student is saying: even though we did not physically attack a live system, the scenarios are still believable because the parts, tools, and attack logic are grounded in real technology.

#### What the reader should understand from this section

- Validation in this thesis means plausibility and defensibility, not experimental proof.
- The student is trying to show that the attacks and controls are realistic enough to be taken seriously.

#### Main ideas to keep in mind while reading

- Validation is qualitative.
- Validation is based on consistency and source support.
- Validation is not penetration testing.

### 2.4 Assumptions

#### What this section says in simple words

- This section lists the assumptions that make the analysis manageable.
- The student says all UAV-to-cloud communication is modeled as IP traffic.
- This simplifies the architecture while keeping the main security meaning.
- The student assumes a public 5G deployment run by a mobile operator, not by the emergency organization itself.
- This matters because it creates a shared-responsibility problem.
- The student also assumes modern 3GPP capabilities, such as UAV-related network functions and slicing-related support.
- A contractual network slice is assumed in the main model.
- The thesis still discusses what happens when that is not fully guaranteed.
- Azure is fixed as the cloud platform.
- The DJI M350 RTK is fixed as the UAV platform.
- The chapter also assumes no malicious insider inside Azure itself.
- It assumes some baseline physical security for the Dock location.
- Finally, it assumes that the organization already has ISO/IEC 27001-style governance in place, so the thesis can focus on technical controls instead of rebuilding governance from zero.

#### What the reader should understand from this section

- The thesis is deliberately bounded.
- It is not claiming to model every UAV, every cloud, every network, or every attacker.
- It is building one detailed analytical case.
- These assumptions strongly shape what the later findings mean.

#### Main ideas to keep in mind while reading

- One concrete UAV platform.
- One concrete cloud context.
- Public 5G as the network reality.
- Strong but not unlimited assumptions about 5G support and organizational governance.

### 2.5 Division of Labor

#### What this section says in simple words

- This section explains how the work was split between two researchers.
- One side focused more on the UAV, 5G network, and threat modeling of those layers.
- That includes the architecture of the drone and radio side, the rogue gNB attack tree, and the mapping of 3GPP-related standards.
- The other side focused more on the cloud, API, web, and standards mapping for the cloud and application side.
- That includes the Azure architecture, the JWT attack tree, and the mapping of NIST, ISO/IEC, and CSA frameworks.
- The section then says several things were joint responsibilities.
- These include combining the threat catalogs, synthesizing the gaps, designing the overall framework, quantifying the risk reduction, and drafting and revising the thesis chapters.
- The student also says joint review sessions were used to keep both sides consistent.

#### What the reader should understand from this section

- The thesis is collaborative, but the analytical streams were divided by domain.
- The key point is that the final outputs were still integrated into one single architecture, one single threat model, and one single framework.

## Quick recap of Chapter 2

- Chapter 2 explains how the thesis was carried out from start to finish.
- It defines a qualitative, structured method.
- It moves from architecture definition to STRIDE threats to attack trees to standards gaps to framework design.
- Validation is analytical rather than experimental.
- Assumptions keep the case focused on a DJI platform, Azure, and public 5G.
- If Chapter 2 is read correctly, the reader should finish it knowing exactly how the thesis was produced and why the later outputs are supposed to be traceable and defensible.