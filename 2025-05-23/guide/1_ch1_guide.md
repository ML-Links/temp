# Guide: Chapter 1 - Introduction

## What this guide does

This guide explains Chapter 1 in simple words. Read it as a plain-language companion to the thesis itself. The point is not only to say what each section is for, but to restate what the student is actually saying, in easier and shorter bullets.

## Chapter 1 in one simple view

- The thesis is about securing drone operations when the drone is controlled through public 5G and a cloud-hosted command-and-control platform.
- The student is not studying a drone alone.
- The student is studying a combined system made of three tightly connected parts: the UAV, the 5G network, and the cloud platform.
- The main argument is that security cannot be handled separately in these three domains.
- The student says current standards and current practice are fragmented.
- The thesis therefore tries to build one cross-layer security view.
- The chapter starts broad, then narrows to the exact research problem, then lists the objectives, questions, scope, contributions, and thesis structure.

## How to read this chapter

- Read it as the promise of the thesis.
- Check whether the problem is stated clearly and early.
- Check whether the chapter explains why this topic matters in practice, not only in theory.
- Check whether the later objectives and research questions really match the problem stated at the start.
- Check whether the chapter stays at introduction level and does not already become a results chapter.

## Detailed reading guide

### 1.1 Background and Motivation

#### What this section says in simple words

- Drones are now used in many real sectors such as emergency response, public safety, inspection, logistics, and city operations.
- In smart cities, they act like flying sensors.
- They can quickly send video and situation information from places that are dangerous or hard for humans to reach.
- This is why they are useful in fires, disasters, security incidents, and search operations.
- The section then shifts from usefulness to risk.
- It says drones are not only IT systems.
- They are cyber-physical systems, so a cyberattack can cause both digital damage and physical harm.
- If an attacker interferes with drone command-and-control, the drone may be hijacked, the mission may fail, or safety may be lost.
- The thesis highlights the command-and-control link as one of the most sensitive parts of the whole system.
- Then the section explains why 5G matters.
- 5G is presented as attractive because it offers low latency, high bandwidth, strong connectivity, and features that fit UAV operations.
- The student also explains that 3GPP has introduced UAV-related support features in newer releases.
- After that, the section adds the cloud side.
- Cloud platforms are used for fleet management, mission planning, storage, and analytics.
- The cloud gives scalability and flexibility, but it also creates new attack surfaces.
- The final move in this section is the key point: once UAV, 5G, and cloud are combined, security becomes a multi-layer problem.
- The student closes by saying this research is timely because 5G adoption is growing, regulations are pushing remote and BVLOS operations, real attacks already exist, and there is still no consolidated end-to-end security framework.

#### What the reader should understand from this section

- The thesis is not trying to prove that drones are useful.
- It uses drone usefulness only to justify why secure operation matters.
- The real focus is the cybersecurity problem created when drone operations depend on public 5G and cloud infrastructure.
- The section wants the reader to accept that this is a real, urgent, and practical problem.

#### Main ideas to keep in mind while reading

- Drones create mission value.
- 5G makes advanced drone operations possible.
- Cloud platforms make control and data handling easier.
- But combining them increases complexity and expands the attack surface.
- Because the system is cyber-physical, security failure may also become safety failure.

### 1.2 Problem Statement

#### What this section says in simple words

- Here the student stops giving general background and states the exact problem.
- The problem is not that standards do not exist.
- The problem is that standards exist separately for different domains, but there is no integrated framework for the combined UAV-5G-cloud system.
- The thesis says responsibilities are split.
- UAV manufacturers care mainly about the drone platform.
- 5G operators care mainly about network integrity and subscriber control.
- Cloud providers care mainly about cloud platform security.
- But the security of the full chain between drone, network, and cloud remains underexplored.
- The student then explains the weakness of each standards family.
- 3GPP protects many network-related aspects, but does not fully solve drone-side issues such as firmware assurance or tamper-proof logging.
- ISO/IEC 27017 and 27018 help with cloud security and privacy, but they do not directly reflect the special constraints of UAV systems.
- NIST SP 800-53 is broad and important, but it assumes conditions that do not fully match public 5G deployments where the UAV operator does not own the network.
- CSA CCM is useful for cloud controls, but it does not cover air-interface and edge-device threats well.
- After that, the section explains the central research gap more sharply.
- It says the real danger is not only isolated weaknesses inside one layer.
- The bigger danger is cross-layer attack paths.
- The thesis gives examples such as hijacking a web session and then using it to send malicious drone commands, or using a rogue base station together with jamming.
- These examples show why single-domain security thinking is not enough.
- The section ends by saying there is no structured and traceable way to identify threats across these layers and map them to suitable controls.
- This is the gap the thesis claims to fill.

#### What the reader should understand from this section

- The thesis problem is an integration problem.
- The issue is not absence of security work.
- The issue is the absence of one defensible security view that covers the whole operating chain.
- The thesis therefore promises a combined method: threat analysis, attack trees, gap analysis, and then a framework.

#### Main ideas to keep in mind while reading

- Existing standards are useful but incomplete when combined.
- Security gaps appear between layers, not only inside layers.
- Cross-layer attacks are a core reason this thesis exists.
- The thesis wants traceability from threat to control.

### 1.3 Research Objectives

#### What this section says in simple words

- This section translates the problem into concrete work packages.
- Objective 1 says the student will build a layered architecture of the whole system.
- This includes components, data flows, trust boundaries, and communication links.
- This architecture is the base for everything that comes later.
- Objective 2 says the student will use STRIDE to identify threats across the architecture.
- The thesis already states that this results in 80 threats across the system.
- Objective 3 says the student will model selected critical threats using attack trees.
- This means the thesis will break down major attacks into smaller attacker steps and show how those steps combine.
- Objective 4 says the student will perform a standards-based gap analysis.
- This means the student will compare the identified threats against 3GPP, NIST, ISO/IEC, and CSA material to see what is covered and what is missing.
- Objective 5 says the student will design a layered cybersecurity framework.
- This framework is said to contain more than thirty controls organized into several layers such as network, edge device, cloud, AI or LLM, and organizational or privacy.
- Objective 6 says the student will validate the framework.
- The validation is described as expert review plus scenario analysis and risk reduction reasoning.

#### What the reader should understand from this section

- The student is giving a full work pipeline.
- First define the system.
- Then identify threats.
- Then model key attacks.
- Then compare against standards.
- Then design controls.
- Then validate whether the controls improve the situation.
- In other words, the thesis moves from system description to threat discovery to security design.

#### Main ideas to keep in mind while reading

- The objectives already reveal the thesis structure.
- Each objective should later appear in a corresponding chapter.
- If a later chapter does not clearly support one of these objectives, the thesis loses coherence.
- This section also shows that the thesis is practical and design-oriented, not only descriptive.

### 1.4 Scope and Boundaries

#### What this section says in simple words

- This section explains what the thesis covers and what it does not cover.
- The student narrows the study to one representative platform: the DJI M350 RTK.
- The thesis also assumes a specific equipment setup, including a 5G communication module, a sensor payload, GNSS, and telemetry support.
- This means the thesis is not claiming universal coverage for every UAV platform.
- The scenario is emergency response, such as fire monitoring or search and rescue.
- This matters because it explains why low latency, reliability, and live data are important.
- The network context is public 5G.
- The organization using the drone does not control the network infrastructure directly.
- The thesis mentions dedicated slicing as an assumption, but it also considers what happens when strong guarantees are not available.
- The cloud platform is Microsoft Azure.
- The thesis lists the main Azure services that support identity, firewalling, storage, communication, and key management.
- This means the framework is grounded in a concrete implementation context rather than a fully abstract one.
- The standards scope is also clearly bounded.
- The gap analysis will focus on selected 3GPP documents, NIST SP 800-53 Rev. 5, ISO/IEC 27017, ISO/IEC 27018, and CSA CCM.
- Other frameworks may be mentioned but are not deeply analyzed clause by clause.
- The threat scope is also limited.
- The thesis focuses on intentional cyberattacks, not mainly on accidental faults, natural disasters, or broad physical-security questions.
- Finally, the validation scope is limited.
- The thesis does not perform live penetration testing or full physical simulation.
- Instead, it uses qualitative validation based on attack trees, gap mapping, expert review, and a plausibility-times-impact model.

#### What the reader should understand from this section

- The student is trying to keep the thesis manageable.
- The work is deep in one carefully defined case, not broad across every possible drone and cloud setting.
- The thesis is analytical, not experimental.
- It claims structured reasoning and traceability, not lab-based proof.

#### Main ideas to keep in mind while reading

- Platform-specific case: DJI M350 RTK setup.
- Scenario-specific case: emergency response.
- Infrastructure-specific case: public 5G plus Azure cloud.
- Standards-specific case: selected major frameworks only.
- Validation-specific case: qualitative and structured, not empirical field testing.

### 1.5 Research Questions

#### What this section says in simple words

- This section turns the objectives into three main questions.
- Research Question 1 asks how command-and-control data and video streams can be secured over public 5G and cloud infrastructure.
- In simple words, this asks how to protect the most important communications moving through the system.
- It includes confidentiality, integrity, and availability.
- It also points to examples of protections such as mutual authentication, data protection, web security, end-to-end encryption, mutual TLS, and token-related protections.
- Research Question 2 asks how communication failures, whether caused by accident or attack, can be handled so that UAV operations stay safe.
- This question is about resilience.
- It is not only asking how to stop attacks.
- It is also asking how the system should behave when something goes wrong.
- The examples include jamming detection, return-to-home logic, offline synchronization, and service-level arrangements with the mobile operator.
- Research Question 3 asks where current standards fail to address the combined UAV-5G-cloud threat landscape, and how those gaps should be addressed.
- This is the standards and governance question.
- It connects directly to the gap analysis and to the final framework.
- It also shows that the thesis is not only about identifying attacks, but also about evaluating whether the current standards environment is enough.

#### What the reader should understand from this section

- The three research questions divide the thesis into three big concerns.
- First: protecting data and control.
- Second: maintaining safe operation under failure or attack.
- Third: checking what standards miss and how to close those gaps.
- Together, these questions define the intellectual core of the thesis.

#### Main ideas to keep in mind while reading

- RQ1 is mainly about security mechanisms.
- RQ2 is mainly about resilience and safe continuity.
- RQ3 is mainly about standards adequacy and gap closure.
- The later chapters should clearly answer all three.

### 1.6 Contribution Statement

#### What this section says in simple words

- This section explains what the thesis claims to add to the field.
- Contribution 1 is a structured catalog of 80 threats mapped to the architecture.
- This means the thesis claims to produce a reusable threat inventory, not only a discussion.
- Contribution 2 is a detailed breakdown of two critical attack scenarios using attack trees.
- This means the thesis wants to show not only that attacks exist, but how they unfold step by step.
- Contribution 3 is a clause-level standards assessment.
- This is important because the thesis is not satisfied with saying standards are weak in general.
- It wants to show specifically where the standards do and do not cover the identified threats.
- Contribution 4 is the layered cybersecurity framework itself.
- The student says the framework contains practical controls across network, edge, cloud, AI or LLM, and organizational or privacy layers.
- Contribution 5 is the claim that these controls reduce the risk level of the most critical threats.
- So the thesis is not only descriptive but also improvement-oriented.
- Contribution 6 is the methodology.
- The student claims the full pipeline can be reused for other cyber-physical systems that also depend on multiple infrastructure layers.
- The section ends by saying the work is relevant to planners, UAV operators, and cybersecurity professionals.

#### What the reader should understand from this section

- The thesis claims both practical and methodological value.
- Practical value means the outputs can help real-world system design and risk reduction.
- Methodological value means the same analytical process could be reused in other similar systems.
- The contributions therefore target both practitioners and researchers.

#### Main ideas to keep in mind while reading

- Threat catalog
- Attack trees
- Standards gap analysis
- Layered framework
- Risk reduction logic
- Repeatable method

### 1.7 Optional: AI Anomaly Detection for UAV Telemetry

#### What this section says in simple words

- This section introduces AI as a possible supporting security mechanism.
- The student is not saying the thesis builds and tests a full AI detection system.
- Instead, the thesis says AI may help detect unusual telemetry or suspicious behavior.
- The idea is that anomaly detection could notice signs of attacks such as spoofing, command abuse, or abnormal system behavior.
- The section also explains where AI monitoring could be placed.
- It could be placed on the UAV, in the 5G environment, or in the cloud platform.
- Each location has different strengths and constraints.
- The student also acknowledges that AI in safety-critical systems has serious challenges.
- These include false positives, adversarial machine learning, and problems in explaining AI decisions clearly.
- The thesis therefore treats AI as a complementary layer, not the center of the whole work.
- The last point is that AI-related controls are proposed conceptually, but the actual building and validation of an AI system is left for future work.

#### What the reader should understand from this section

- AI is included as a supporting idea, not as the main contribution.
- The core thesis remains threat analysis, standards analysis, and framework design.
- This section mainly shows awareness of an emerging topic that may strengthen future security monitoring.

#### Main ideas to keep in mind while reading

- AI is secondary here.
- AI is conceptual here.
- AI is future-facing here.
- The thesis should not depend on AI to justify its main value.

### 1.8 Structure of the Thesis

#### What this section says in simple words

- This final section tells the reader how the rest of the thesis is organized.
- Chapter 2 explains how the study was carried out.
- It covers the research design, methodology steps, validation approach, assumptions, and division of labor.
- Chapter 3 presents the reference architecture and mission communication flow.
- This chapter gives the concrete system picture on which the rest of the security analysis depends.
- Chapter 4 gives the theoretical background.
- It explains the smart-city and UAV context, cybersecurity concepts, standards, and threat-modeling methods.
- Chapter 5 presents the analytical results.
- It contains the 80-threat STRIDE catalog, the attack trees, and the standards-based gap analysis.
- Chapter 6 moves from analysis to interpretation and solution discussion.
- It introduces the final framework, discusses how well it works, explains risk reduction, and addresses the research questions.
- Chapter 7 gives the final summary of the whole thesis.
- It restates what was done and why it matters.

#### What the reader should understand from this section

- The thesis follows a logical build-up.
- Introduction first.
- Method next.
- System description and theory after that.
- Results and analysis after that.
- Discussion, conclusions, and summary at the end.
- This section helps the reader see where each promised part of the work will appear.

## Quick recap of Chapter 1

- The thesis studies how to secure a cloud-hosted UAV command-and-control system that uses public 5G.
- The student argues that current standards are fragmented and do not solve the whole cross-layer problem.
- The thesis therefore builds a reference architecture, identifies threats, models key attacks, checks standards gaps, designs a layered framework, and validates it qualitatively.
- The work is bounded to a specific emergency-response scenario, a DJI platform, Azure cloud, public 5G, and selected standards.
- The chapter promises practical outputs and a reusable method.
- If Chapter 1 is read correctly, the reader should finish it knowing exactly what the thesis problem is, why it matters, what the thesis will do, and how the rest of the document is organized.