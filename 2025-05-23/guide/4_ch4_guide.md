# Guide: Chapter 4 - Theoretical Background

## What this guide does

This guide explains Chapter 4 in simple words. It follows the chapter section by section and tells you what the student is trying to establish as the theory base for the later security analysis.

## Chapter 4 in one simple view

- Chapter 4 gives the conceptual background behind the thesis.
- It starts by placing UAVs inside smart-city use cases.
- Then it explains the layered ICT model of a smart city.
- After that, it reviews key cybersecurity principles.
- Then it discusses threats and vulnerabilities specific to UAV systems.
- Then it introduces the standards families used later in the gap analysis.
- Then it explains STRIDE and attack trees as the analytical methods.
- Finally, it briefly introduces AI anomaly detection as a supporting future-oriented idea.

## How to read this chapter

- Read it as the theory toolbox of the thesis.
- The student is not yet presenting results here.
- The student is explaining the concepts needed to understand why the later analysis is structured the way it is.
- The key question to keep in mind is: how does each theory piece help explain the UAV-5G-cloud problem?

## Detailed reading guide

### 4.1 UAV Use Cases in Smart Cities

#### What this section says in simple words

- The student starts by showing that UAVs are useful in many smart-city contexts.
- The purpose is not only to talk about drones in general.
- The student wants to show that UAVs are increasingly part of city operations and therefore bring real cybersecurity relevance.
- The deeper point is that UAVs are mobile, sensor-rich, and network-dependent, so they interact with many parts of a city's ICT environment.

### 4.1.1 Public Safety and Law Enforcement

#### What this subsection says in simple words

- Here the student explains that drones can help with surveillance, event monitoring, border observation, accident response, suspect tracking, and infrastructure protection.
- The value of the drone is its aerial perspective and real-time visual monitoring.
- The cybersecurity importance is that this use case depends on live communication, real-time data, and operational trust.

### 4.1.2 Emergency Response

#### What this subsection says in simple words

- This is the core use case of the thesis.
- The student explains that drones are very useful in disaster response, firefighting, search and rescue, and medical support.
- The key reason is that they can enter dangerous environments where human responders would face high risk.
- Thermal imaging, situational awareness, and quick scanning of large areas are central benefits.
- The student is using this subsection to justify why secure and reliable UAV operation matters in life-critical missions.

### 4.1.3 Infrastructure Inspection

#### What this subsection says in simple words

- The student explains that drones can inspect bridges, pipelines, utilities, buildings, and other structures more safely and cheaply than manual inspection.
- The payload sensors help detect defects such as cracks, leaks, or corrosion.
- This subsection broadens the argument by showing that UAVs are used in other critical domains too.

### 4.1.4 Environmental Monitoring

#### What this subsection says in simple words

- The student says UAVs can be used to measure air quality, noise, pollution, and weather-related conditions.
- This means drones can act as mobile environmental sensing platforms.
- The relevance for the thesis is that UAV operations often involve collection and transfer of rich sensor data.

### 4.1.5 Urban Planning and Traffic Management

#### What this subsection says in simple words

- The student explains that drones can assist in monitoring congestion, road conditions, traffic incidents, and possibly logistics or urban mobility services.
- The broader message is that UAVs may become part of regular urban digital infrastructure rather than rare special tools.

### 4.1.6 Urban Agriculture

#### What this subsection says in simple words

- This subsection shows another use case: drones supporting precision agriculture through imaging and targeted treatment.
- Even though this is less central to the thesis, it helps the student show that UAVs are increasingly tied to data-driven operations.

### 4.1.7 Healthcare

#### What this subsection says in simple words

- The student explains that UAVs can deliver medicine and diagnostic samples, support disaster medicine, and assist with health-oriented monitoring tasks.
- The broader message is that UAV use can become mission-critical and time-sensitive.

### 4.1.8 Common Dependencies Across Use Cases

#### What this subsection says in simple words

- This is the synthesis point of Section 4.1.
- The student says all these UAV use cases depend on reliable low-latency communication, predictable QoS, secure transmission of command and data, and cloud-based storage or analytics.
- This is an important transition.
- It connects the general use-case survey to the specific technical problem of the thesis.

#### What the reader should understand from Section 4.1

- The student is showing that UAVs are operationally useful across many city functions.
- More importantly, these use cases share infrastructure dependencies.
- Those shared dependencies are exactly why the UAV-5G-cloud combination becomes a security issue worth studying.

### 4.2 Smart City ICT Infrastructure

#### What this section says in simple words

- This section introduces a layered smart-city ICT model.
- The point is to show where the UAV system fits inside a larger city technology stack.
- The student uses a five-layer model running from data collection up to end-user applications.
- The deeper idea is that UAV cybersecurity should not be seen only as a drone problem.
- It should be understood as part of a broader digital infrastructure.

### 4.2.1 Layer 1: Data Acquisition

#### What this subsection says in simple words

- This layer contains sensors and devices that gather real-world data.
- The student places the UAV here as a mobile sensing device.
- The key message is that the drone is not only a vehicle.
- It is also a data-acquisition platform feeding upper layers of the city system.

### 4.2.2 Layer 2: Communication

#### What this subsection says in simple words

- This layer moves data between sensing and higher-level processing.
- The student discusses different networking technologies and emphasizes public 5G as the crucial communication layer for this thesis.
- The reason is that 5G supports wide-area BVLOS communication and HD data transport.

### 4.2.3 Layer 3: Computing (Processing and Storage)

#### What this subsection says in simple words

- This layer stores and processes the data gathered by sensors.
- The student explains that cloud and possibly edge computing are used here.
- In the thesis case, Azure represents this layer.
- The key message is that the UAV does not carry all intelligence locally.
- It depends on external computing and storage resources.

### 4.2.4 Layer 4: Service

#### What this subsection says in simple words

- This layer provides the service environment that supports applications.
- It includes cloud service models, middleware, and managed capabilities.
- In simple terms, it is the layer that lets the application run without the operator managing every underlying technical detail.

### 4.2.5 Layer 5: Application

#### What this subsection says in simple words

- This is the user-facing layer.
- The student explains that applications create usable value for citizens and operators.
- In the thesis case, FlightHub 2 is the main application used by the operator through a browser.

#### What the reader should understand from Section 4.2

- The student is placing the UAV system inside a layered smart-city environment.
- This helps justify why later analysis looks at multiple layers rather than only the drone.
- The UAV is just one part of a larger digital chain.

### 4.3 Cybersecurity Fundamentals

#### What this section says in simple words

- This section introduces the main security concepts used later in the thesis.
- The student is building a vocabulary for understanding threats, controls, trust, and risk.

### 4.3.1 The CIA Triad

#### What this subsection says in simple words

- Confidentiality means sensitive information should not be exposed to unauthorized parties.
- In this thesis, that includes video, thermal images, telemetry, and mission data.
- Integrity means data and commands should not be changed improperly.
- In the UAV context, this matters especially for flight commands, GNSS data, and recorded evidence.
- Availability means the system must remain accessible and functional when needed.
- In an emergency-response mission, loss of communication or service can directly affect mission safety.
- The student is showing that UAV security is not only about privacy or secrecy.
- It is also about safe command execution and continuous availability.

### 4.3.2 The AAA Triad

#### What this subsection says in simple words

- Authentication means each entity must prove who it is.
- Authorization means each authenticated actor should only be allowed to do what its role permits.
- Accounting means important actions must be logged so the system can support audit and forensic review.
- The student applies this to the UAV, Dock, operator, Azure services, and internal system identities.

### 4.3.3 Defense-in-Depth

#### What this subsection says in simple words

- The student explains defense-in-depth as multiple layers of protection.
- The system should not collapse because one control fails.
- The section gives examples across physical, network, application, data, and human layers.
- The thesis later uses this concept as the backbone of the final framework structure.

### 4.3.4 Zero Trust

#### What this subsection says in simple words

- Zero trust means the system should not trust something just because it is inside a network.
- Every access request should be verified continuously.
- This fits the thesis well because the UAV system spans public 5G, the internet, and cloud infrastructure.
- The student uses zero trust to support the idea that all communication paths must be authenticated, authorized, and encrypted.

### 4.3.5 Secure by Design / Privacy by Design

#### What this subsection says in simple words

- Secure by design means security choices should be built into the architecture early, not added later.
- Privacy by design means privacy protection should also be built into the system from the beginning.
- The student connects this to topics such as strong authentication, encryption, and privacy-preserving treatment of UAV imagery.

### 4.3.6 Risk Management Terminology

#### What this subsection says in simple words

- The student defines key terms such as threat, vulnerability, impact, plausibility, risk, and risk treatment.
- This is important because the thesis later uses these words in a structured way.
- The goal here is to make sure that later scoring and discussion use consistent meaning.

#### What the reader should understand from Section 4.3

- This section gives the conceptual language for the later chapters.
- CIA explains what must be protected.
- AAA explains how access and accountability should work.
- Defense-in-depth and zero trust explain how layered protection should be thought about.
- Risk terminology explains how later analysis is organized.

### 4.4 UAV-Specific Threats and Vulnerabilities

#### What this section says in simple words

- This section shifts from general security theory to UAV-specific security problems.
- The student explains that UAVs are cyber-physical systems and are exposed through software, wireless links, cloud dependence, and limited onboard resources.

### 4.4.1 Cyber Threats to the UAV System

#### What this subsection says in simple words

- The student discusses several categories of attack.
- First, there are operator-side threats such as malware, phishing, and session hijacking affecting the browser or console.
- Second, there are communication-link threats across DPP, 5G, VPN, and MQTT paths.
- Third, there are firmware and supply-chain threats, where malicious or compromised updates can create persistent compromise.
- Fourth, there are cloud and fleet-management threats, where compromise of FlightHub 2 or cloud permissions can affect multiple drones.
- Fifth, there are insider threats involving legitimate users misusing their access.
- In simple words, the student is saying UAV risk is distributed across multiple layers, not just the aircraft itself.

### 4.4.2 UAV Inherent Cyber Vulnerabilities

#### What this subsection says in simple words

- Here the student focuses on built-in weaknesses common to UAV platforms.
- These include weak or unverifiable encryption, insufficient firmware integrity assurance, predictable autonomy logic, and poor forensic readiness.
- The student is showing that drone platforms may prioritize performance, weight, and cost ahead of strong security.
- This means outside layers such as 5G and cloud controls may need to compensate for native UAV weakness.

#### What the reader should understand from Section 4.4

- The thesis is grounding the later threat model in known UAV security problems.
- Both external attacks and inherent platform weaknesses matter.
- This section prepares the reader to accept why a multi-layer control framework will later be proposed.

### 4.5 Standards Overview

#### What this section says in simple words

- This section introduces the standards families that will later be checked against the threat landscape.
- The student is not yet presenting gaps.
- The student is explaining what each framework covers and why it matters.

### 4.5.1 3GPP Standards for UAS

#### What this subsection says in simple words

- The student explains that 3GPP provides the mobile-network standards relevant to UAV operation over public 5G.
- The thesis uses a set of 13 specifications and reports as the 3GPP baseline.
- The deeper point is that the 5G side of the system is governed by a large standards ecosystem, not by one single document.

### 4.5.2 ISO/IEC 27017 and ISO/IEC 27018

#### What this subsection says in simple words

- ISO/IEC 27017 is used for cloud-specific security controls and shared-responsibility thinking.
- ISO/IEC 27018 is used for privacy protection of personal data in public-cloud settings.
- The student applies these to FlightHub 2 on Azure and to sensitive UAV data such as video and telemetry.

### 4.5.3 NIST SP 800-53 Rev. 5

#### What this subsection says in simple words

- The student explains that NIST SP 800-53 is a broad security and privacy control catalog.
- The thesis focuses on ten control families most relevant to this case.
- In simple words, NIST gives a general control language for thinking about access, audit, configuration, incident response, communication security, and supply chain management.

### 4.5.4 CSA Cloud Controls Matrix v4.1

#### What this subsection says in simple words

- The student introduces CSA CCM as a cloud-focused control framework.
- It is especially relevant for cloud operations, service governance, and operational control domains.
- In this thesis it is used to evaluate cloud-native and edge-related concerns in the UAV system.

#### What the reader should understand from Section 4.5

- Each standards family covers a different part of the problem.
- 3GPP mainly covers the network side.
- ISO/IEC 27017 and 27018 mainly cover cloud security and privacy.
- NIST gives a broad control framework.
- CSA CCM adds cloud-focused operational coverage.
- The thesis later uses all of them because no single framework covers the whole UAV-5G-cloud stack.

### 4.6 STRIDE and Attack Tree Methodology

#### What this section says in simple words

- This section explains the analytical methods from a theory perspective.
- Chapter 2 already explained how the methods are used in the thesis workflow.
- Here Chapter 4 explains what those methods mean conceptually.

### 4.6.1 STRIDE Threat Modelling

#### What this subsection says in simple words

- The student explains STRIDE as a structured way to identify six kinds of threats: spoofing, tampering, repudiation, information disclosure, denial of service, and elevation of privilege.
- The method is applied to the eight components defined earlier in Chapter 3.
- The chapter says this produces a catalog of 80 threats.
- The student also says STRIDE is used iteratively because UAV systems change state during operation and span multiple layers.

### 4.6.2 Attack Tree Methodology

#### What this subsection says in simple words

- Attack trees are explained as a way to break high-level attack goals into smaller sub-goals and atomic actions.
- AND nodes mean all child steps are necessary.
- OR nodes mean one of several possible paths is enough.
- Leaf nodes are evaluated by difficulty, detection, and access.
- The student then links this concept to the two thesis scenarios: rogue gNodeB forced landing and stolen JWT command injection.
- The main purpose is to show how cross-layer attacks can be decomposed clearly.

#### What the reader should understand from Section 4.6

- STRIDE gives the broad threat map.
- Attack trees give detailed adversary paths.
- Together they support the type of layered analysis the thesis wants to perform.

### 4.7 AI Anomaly Detection Concepts

#### What this section says in simple words

- This final section explains anomaly detection as a possible supporting technique.
- The student describes it as a way to detect unusual patterns that may signal attacks, especially when static rules may miss them.
- Examples include GPS spoofing or suspicious telemetry behavior.
- The student mentions several ML approaches such as autoencoders, isolation forests, and recurrent models.
- The section also says detection could happen on the UAV, in the network layer, or in the cloud platform.
- However, the thesis treats this only conceptually.
- It is not a built and validated system in this work.

#### What the reader should understand from this section

- AI anomaly detection is included as an optional complementary idea.
- It is not the main analytical foundation of the thesis.
- The real core remains UAV security theory, standards, STRIDE, attack trees, and the layered system view.

## Quick recap of Chapter 4

- Chapter 4 gives the theoretical background for the thesis.
- It starts with smart-city UAV use cases and the smart-city ICT layers.
- It then explains core cybersecurity concepts and UAV-specific security problems.
- After that, it introduces the standards families used later in the gap analysis.
- It also explains STRIDE and attack trees as the main analytical methods.
- It ends with a brief conceptual note on AI anomaly detection.
- If Chapter 4 is read correctly, the reader should finish it understanding why the thesis treats the UAV system as a multi-layer security problem and why the later methods and standards were chosen.