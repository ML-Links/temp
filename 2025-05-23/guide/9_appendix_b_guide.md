# Guide: Appendix B - Clause-Level Standards Gap Mapping

## What this guide does

This guide explains Appendix B in simple words. It tells you what the clause-level mapping is trying to prove and what each standards block contributes to that proof.

## Appendix B in one simple view

- Appendix B is the detailed standards evidence behind Chapter 5.
- It maps specific threats to specific clauses in four framework families.
- For each entry, the appendix records the threat, the clause, the control requirement, the verdict, and the explanation of the gap.
- In simple words, this appendix shows exactly why the thesis says current standards are incomplete for the UAV-5G-cloud case.

## How to read this appendix

- Read it as a structured evidence log, not as narrative prose.
- The appendix is grouped by standards family.
- Inside each family, it shows where coverage is missing, partial, or too weak for the actual threat landscape.

## Detailed reading guide

### B.1 3GPP specifications and technical reports

- This is the biggest standards block in the appendix.
- It focuses on the public-5G and UAS side of the problem.
- The repeated theme across these entries is that many protections are optional, incomplete, inherited from general 5G assumptions, or left to vendor and operator implementation.

#### B.1.1 TS 22.125

- This subsection shows that high-level UAS support requirements exist, but several security expectations remain written as should rather than mandatory shall requirements.
- The gaps here affect end-to-end C2 protection, remote identity trust, UAV identification binding, emergency QoS guarantees, fallback communications, and airborne-device hardening.

#### B.1.2 TS 33.125

- This subsection focuses on UAS-specific security aspects.
- The main pattern is that null ciphering, optional integrity, optional UUAA, missing standardized secure updates, and weak standard coverage for the UAV-to-Dock side leave important protections open.
- In simple words, this block says even UAS-focused 5G security still leaves key implementation decisions unresolved.

#### B.1.3 TS 33.501

- This subsection targets the core 5G security architecture.
- The main theme is that user-plane integrity and cipher strength are not enforced strongly enough for UAV C2 needs.
- It also shows weak identity binding, optional slice-specific protections, and no UAV-specific secure failover model.
- This is one of the strongest appendix blocks supporting the rogue gNB and C2 tampering concerns.

#### B.1.4 TS 23.256

- This subsection deals with connectivity, identification, tracking, and UAS network-function logic.
- The main message is that pairing, identity, continuity, and tracking support exist, but they do not fully secure a cloud-relayed multi-hop architecture like the thesis case.

#### B.1.5 TS 33.256

- This subsection covers the normative UAS-security layer.
- The repeated pattern is that many protections are still policy-based, inherited from weaker lower-layer assumptions, or missing real-time revocation and stronger binding requirements.

#### B.1.6 TS 23.255

- This subsection focuses on application-layer UAS support.
- Its key message is that reliable delivery is discussed, but message-level integrity, replay protection, per-command identity binding, and stronger confidentiality assumptions are not fully standardized.

#### B.1.7 TS 24.257

- This subsection moves into protocol details.
- The main theme is that authentication tokens, signatures, replay protections, and real-time revocation are often optional or incomplete at the protocol level.

#### B.1.8 TS 23.501

- This subsection covers broader 5G system-architecture assumptions.
- The gaps here show that slice isolation, redundancy, handover, and aerial identity handling are still grounded in general mobile-system assumptions rather than mission-critical UAV needs.

#### B.1.9 TS 23.527

- This subsection addresses restoration and resilience.
- The key point is that recovery is treated as best-effort restoration, without hard UAV-specific guarantees for timing, security-context preservation, or prioritized recovery.

#### B.1.10 TR 33.891

- This is a study-report block.
- The pattern here is important: the report recognizes many problems, but recognition is not the same as mandatory protection.
- RF attack mitigation, DAA security, inter-MNO continuity, PKI lifecycle, privacy, and monitoring are discussed but not fully standardized.

#### B.1.11 TR 23.754

- This block shows study-level UAS connectivity and tracking findings.
- The recurring message is that direct models, one-to-one assumptions, and incomplete security binding leave cloud-relayed, multi-domain UAV operations insufficiently protected.

#### B.1.12 TR 22.829

- This subsection highlights enhancement studies for UAV support.
- The key gap is that performance goals are discussed more clearly than security goals.
- Security KPIs, degraded-security operation, and spoofing-related navigation protections are not fully defined.

#### B.1.13 TR 23.700-58

- This later study block extends the same pattern into UAS and UAM evolution.
- The main theme is that future-oriented airborne ecosystem issues are visible, but still not standardized strongly enough for practical deployment security.

#### What the reader should understand from B.1 overall

- The 3GPP family is essential but incomplete for the thesis problem.
- The major recurring weaknesses are optionality, incomplete end-to-end protection, weak identity binding, insufficient message-level integrity, and limited mission-critical resilience guarantees.

### B.2 NIST SP 800-53 Rev. 5

- This block shows how a broad security control catalog maps only partially to the UAV-5G-cloud case.
- The main pattern is not that NIST is weak in general.
- The problem is that NIST assumes organization-controlled IT environments more than shared multi-domain public-network cyber-physical systems.

#### B.2.1 Access Control

- The gaps here show that enterprise-style access control does not fully fit public-network slices, unattended field devices, MQTT topic authorization, or physically exposed UAV assets.

#### B.2.2 Awareness and Training

- This block shows that generic training models do not capture UAV-specific attack indicators, cloud-UAV administrative roles, cyber-physical drills, or mission-control misuse patterns.

#### B.2.3 Audit and Accountability

- The gaps here show that standard audit logic does not fully cover externally operated network visibility, MQTT event content, cross-domain correlation, or container-aware forensic logging.

#### B.2.4 Security Assessment and Authorization

- This subsection shows that assessment and authorization models assume one owner or one authorizing structure.
- That assumption breaks down when cloud, MNO, UAV vendor, and operator all share part of the system.

#### B.2.5 Configuration Management

- These gaps show that baseline control, drift management, and change control are harder in vendor-locked devices, cloud-shared systems, and containerized services than in standard enterprise IT.

#### B.2.6 Contingency Planning

- This block shows that redundancy and recovery planning assume infrastructure the organization can directly shape.
- Public 5G links, aviation-safety constraints, and carrier dependency are not covered strongly enough.

#### B.2.7 Incident Response

- The incident response gaps show that standard IT incident taxonomy does not fully cover forced landing, jamming, air-interface abuse, or evidence preservation for field UAV events.

#### B.2.8 System and Communications Protection

- This is one of the most important NIST subsections.
- It shows that boundary protection, wireless protection, token authenticity, key lifecycle, replay protection, and segmentation assumptions need stronger adaptation for the UAV case.

#### B.2.9 System and Information Integrity

- These gaps show that firmware trust, container monitoring, runtime-state integrity, endpoint criticality, and proprietary-protocol verification are not handled deeply enough by generic models.

#### B.2.10 Supply Chain Risk Management

- This block shows that the supply-chain model becomes difficult when components are closed-source, foreign-manufactured, field-deployed, and supported through commercial reseller channels.

#### What the reader should understand from B.2 overall

- NIST gives valuable control language, but it is not naturally fitted to this multi-party UAV-5G-cloud environment.
- The main weakness is mismatch between enterprise assumptions and real cyber-physical deployment conditions.

### B.3 ISO/IEC 27017:2015

- This block focuses on cloud-security responsibility.
- The main message is that shared responsibility is defined mainly between cloud provider and customer.
- The thesis case needs a wider model that also accounts for the mobile operator and field devices.
- Other gaps concern containerized C2 applications, cross-boundary monitoring, telecom dependency in continuity planning, and field-device key lifecycle.

### B.4 ISO/IEC 27018:2025

- This block focuses on privacy in public-cloud processing.
- The key message is that standard cloud privacy thinking does not fully fit real-time aerial imagery, telemetry, transient data capture, geolocation sensitivity, and the mobile operator's position in the processing chain.

### B.5 CSA Cloud Controls Matrix v4.1

- This block focuses on cloud-control coverage for operational reality.
- The repeated theme is that cloud control models often stop at the cloud boundary.
- The thesis case needs stronger treatment of public mobile networks, unattended edge devices, MQTT-based command paths, airborne data minimization, OT-style supply chain issues, wireless continuity loss, and aviation-oriented incident handling.

## What this appendix tells you overall

- Appendix B is the formal proof that standards coverage is fragmented.
- 3GPP leaves important radio and UAS issues partly optional.
- NIST gives broad controls but assumes enterprise-style ownership and control.
- ISO/IEC cloud and privacy standards help, but they do not fully capture the UAV edge and telecom chain.
- CSA adds cloud-operational thinking, but still does not close the whole end-to-end UAV-5G-cloud problem.

## Quick recap

- Appendix B is the clause-level standards evidence behind Chapter 5.
- It maps individual threats to individual standards clauses and explains why coverage is partial or missing.
- The appendix supports the thesis claim that the problem is not a total absence of standards, but a fragmented standards landscape with recurring end-to-end gaps.
- If Appendix B is read correctly, the reader should understand exactly why the thesis says a compensating layered framework is needed on top of existing standards.