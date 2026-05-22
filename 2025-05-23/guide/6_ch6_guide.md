# Guide: Chapter 6 - Discussion and Conclusions

## What this guide does

This guide explains Chapter 6 in simple words. It tells you what the student's final framework contains, what risks remain, how the student interprets the results, and how the research questions are answered.

## Chapter 6 in one simple view

- Chapter 6 turns the Chapter 5 findings into a security framework and an interpretation.
- The student groups the controls into five layers: 5G network, edge device, cloud platform, AI or LLM, and organizational or privacy.
- Then the student explains residual risks, key findings, risk reduction, limitations, future work, and the final answers to the research questions.
- In simple words, this chapter says: based on the threats and standards gaps, this is what should be done, this is what improves, and this is what still remains imperfect.

## How to read this chapter

- Read it as the response chapter.
- The earlier chapters built the problem and the evidence.
- This chapter says what the student wants the reader to conclude from that evidence.
- Keep track of which controls respond to which threats and gaps.

## Detailed reading guide

### 6.1 Introduction

#### What this section says in simple words

- The student opens by reminding the reader what Chapter 5 produced: STRIDE threats, two attack trees, and standards gaps.
- The section then says Chapter 6 will translate these into a layered framework.
- The student explains that the framework will include compensating controls, architectural improvements, and organizational measures.
- The chapter is therefore positioned as the bridge from analysis to solution discussion.

#### What the reader should understand from this section

- Chapter 6 is not independent from Chapter 5.
- It is meant to be the practical interpretation of the findings.

### 6.2 Proposed Cybersecurity Framework

#### What this section says in simple words

- The student presents the main security framework of the thesis.
- The key idea is defense-in-depth.
- Because the operator does not control every part of the 5G and cloud infrastructure, the system needs compensating controls across several layers.
- Each control is given an identifier and linked to specific threats or gaps.

### 6.2.1 5G Network Layer Controls

#### What this subsection says in simple words

- These controls try to compensate for weakness in the public 5G environment.
- R-1 adds application-layer encryption and integrity so command traffic is still protected even if radio-level protections are insufficient.
- R-2 strengthens GNSS trust through multi-constellation and fallback logic.
- R-3 adds onboard jamming detection.
- R-4 defines deterministic safe behavior when the C2 link is lost.
- R-5 moves part of the solution into the contractual relationship with the mobile network operator through service and security guarantees.
- In simple words, the student is saying the public network cannot be trusted blindly, so higher-layer and operational compensations are needed.

### 6.2.2 Edge Device Layer Controls (UAV and Dock)

#### What this subsection says in simple words

- These controls harden the UAV and Dock side.
- They include secure boot, runtime integrity checking, mutual certificate authentication, encrypted local storage, signed logs, no default credentials, and offline state synchronization.
- The student is focusing here on making the physical and near-edge parts of the system harder to impersonate, tamper with, or misuse.
- The Dock is particularly important because it sits between the drone and the cloud path.

### 6.2.3 Cloud Platform Layer Controls (Azure)

#### What this subsection says in simple words

- These controls protect the Azure-hosted FlightHub 2 environment.
- The student includes short-lived bound JWTs, logging, privileged management controls, WAF, DDoS protection, MQTT broker hardening, Private Link, strict TLS use, certificate rotation, and Docker container hardening.
- In simple words, this layer is trying to protect the web, token, service, and runtime side of the command-and-control platform.

### 6.2.4 AI / LLM Agent Layer Controls

#### What this subsection says in simple words

- This layer deals with AI-related risk if AI or LLM capabilities are used for planning or monitoring.
- The controls cover input validation, output safety checks, audit trails, adversarial testing, model provenance, and behavior monitoring.
- The student treats this as an additional layer, not the core of the whole thesis.

### 6.2.5 Organizational and Privacy Controls

#### What this subsection says in simple words

- These controls move beyond technical configuration into governance and operational process.
- They include privacy impact assessment, real-time privacy redaction, data-processing agreements, software bill of materials, vulnerability disclosure agreements, UAV-specific incident response, supply-chain risk management, and coordination with the mobile operator.
- The student is showing that technical security alone is not enough for this system.

### 6.2.6 Residual Risks

#### What this subsection says in simple words

- This subsection admits that the framework does not remove all risk.
- The student lists remaining risks such as RF jamming, physical theft or tampering, zero-day issues in Azure-managed services, advanced prompt injection, secure-element extraction by very strong attackers, and mobile operator SLA failure.
- The student then explains why these risks are accepted or only partially transferable.
- In simple words, this section says: the framework improves the system, but some risks remain and must be managed rather than eliminated.

#### What the reader should understand from Section 6.2

- The framework is layered because the system problem is layered.
- The student is trying to show coverage across radio, edge, cloud, AI, and governance.
- The residual-risk section is important because it prevents the framework from sounding unrealistically perfect.

### 6.3 Key Findings from the Analysis

#### What this section says in simple words

- This section interprets what the framework means against the previously identified threats.
- The student argues that specific critical threats are reduced by specific controls.
- Rogue gNB exposure is addressed by application-layer protection.
- RF jamming remains difficult to prevent, but safer handling is introduced.
- JWT theft is reduced by stronger token design.
- Cloud threats such as SQL injection, DDoS, and container escape are tied to cloud-layer controls.
- The student also restates the six major gap themes and shows how the proposed framework answers them.

### 6.3.1 Effectiveness of the Proposed Cybersecurity Framework

#### What this subsection says in simple words

- The student explains why the framework should improve the security posture.
- The argument is not based on live deployment proof.
- It is based on analytical linkage between threats, controls, and gap categories.
- In simple words, the student is saying: if these controls are applied, the earlier attack paths become harder or less harmful.

### 6.3.2 Risk Coverage

#### What this subsection says in simple words

- Here the student summarizes how much of the major threat landscape is addressed.
- The strongest claim is that most of the previously critical threats are reduced to medium or low levels.
- RF jamming remains the most difficult residual issue.

### 6.3.3 Practical Relevance

#### What this subsection says in simple words

- This part explains why the framework matters beyond theory.
- The student says the controls are concrete and implementable, not only conceptual.
- The chapter also says the recommendations are relevant to UAV operators, cloud architects, and standards bodies.

#### What the reader should understand from Section 6.3

- The student wants the framework to be seen as practical, not merely academic.
- At the same time, the support for effectiveness remains analytical rather than empirical.

### 6.4 Risk Score Interpretation and Security Posture Improvement

#### What this section says in simple words

- This section quantifies the claimed improvement.
- The student uses a five-point plausibility score and a five-point impact score.
- Multiplying them gives a risk score between 1 and 25.
- The chapter then compares pre-control and post-control scores for eight major threats.
- The student claims reductions between 40 percent and 75 percent.
- Rogue gNB risk, JWT theft risk, default credential risk, and several others are shown as reduced.
- RF jamming still remains more difficult than the others, though its impact is reduced because the UAV can fail safely.

#### What the reader should understand from this section

- This is the thesis's strongest attempt to show measurable improvement.
- The numbers are not incident statistics.
- They are structured analytical scores used to compare the before and after picture.

### 6.5 Limitations of the Research

#### What this section says in simple words

- The student acknowledges several limitations.
- The analysis is tied to one DJI-Azure-5G case and may not generalize fully.
- The framework review is document-based and not supported by live penetration testing.
- Some important elements remain assumed, such as third-party hardware compatibility and some network-slice conditions.
- The results reflect the technologies and standards available at the time of writing.
- Some threats, especially nation-state or insider cases, are not fully modeled.
- AI-related controls are prospective rather than validated in operation.

#### What the reader should understand from this section

- The student is setting realistic boundaries around the claims.
- The thesis offers a structured framework, not a final universally proven security solution.

### 6.6 Future Research Directions

#### What this section says in simple words

- This section says what should be done next beyond the thesis.
- The student suggests empirical validation with a real testbed.
- Multi-UAV and swarm settings are proposed as future scope.
- Other UAV platforms and other cloud providers should be studied for generalizability.
- More quantitative risk models could be explored.
- AI or ML security for the aerial domain could be tested more deeply.
- Regulatory integration and real-world pilot deployment are also proposed.
- Supply-chain analysis is another future area.

#### What the reader should understand from this section

- The student sees the thesis as a starting framework, not the end of the topic.
- The next steps mainly involve broader validation, broader scope, and deeper empirical work.

### 6.7 Conclusions

#### What this section says in simple words

- The student closes by restating the main contributions: threat model, multi-standard gap analysis, layered framework, quantified risk reduction, and repeatable method.
- The chapter then gives direct answers to the three research questions.
- For RQ1, the answer is that command, control, telemetry, and video need layered protection across radio, identity, messaging, cloud, and runtime controls.
- For RQ2, the answer is that communication failures cannot be removed completely, but they can be handled through detection, deterministic fallback, and organizational coordination.
- For RQ3, the answer is that current standards leave recurring thematic gaps, but a compensating framework can close many of them.
- In simple words, the student concludes that public-5G UAV emergency systems can become safer and more defensible, but only through a carefully layered approach.

## Quick recap of Chapter 6

- Chapter 6 turns the earlier findings into a layered security framework.
- It explains how the controls are distributed across network, edge, cloud, AI, and organizational layers.
- It admits that some residual risks remain.
- It interprets the analytical results and presents a quantified before-and-after security picture.
- It also states the thesis limitations, future work, and final answers to the research questions.
- If Chapter 6 is read correctly, the reader should finish it knowing what the thesis recommends, what improvement it claims, and where the remaining uncertainty still lies.