# Guide: Chapter 3 - Current State Analysis

## What this guide does

This guide explains Chapter 3 in simple words. It summarizes the actual system being studied, how the parts connect, how messages move during a mission, and where the trust boundaries sit.

## Chapter 3 in one simple view

- This chapter defines the reference system used in the thesis.
- The system is built around a DJI drone, a Dock, a public 5G network, a cloud-hosted FlightHub 2 server on Azure, and a web-based operator.
- The chapter is important because later threats, attack trees, and standards gaps are all tied to this architecture.
- In simple words, Chapter 3 tells the reader: this is the exact system we are analyzing, this is how it communicates, and these are the weak points where trust changes.

## How to read this chapter

- Read it as the technical picture of the thesis case.
- Keep track of who talks to whom.
- Keep track of which links are wireless, which are internet-based, and which stay inside Azure.
- Pay special attention to the Dock, the browser, the FlightHub 2 server, the VPN path, and the trust boundaries.

## Detailed reading guide

### 3.1 Introduction

#### What this section says in simple words

- The student opens by saying UAV emergency response depends on more than the drone itself.
- It depends on 5G for connectivity and on cloud infrastructure for command and control.
- The student says this combination makes BVLOS operation possible, but also creates a complex attack surface.
- The purpose of the chapter is therefore to describe the current system in enough detail that later threat analysis can be done properly.
- The section also says the chapter will end with trust boundaries and data flows.
- This is an important methodological signal: the chapter is not only descriptive, it is preparing the exact input for later security analysis.

#### What the reader should understand from this section

- Chapter 3 is the system map of the thesis.
- If the architecture is unclear here, the rest of the thesis becomes weak.
- The student is saying that security analysis must begin with a clear model of the real components and their connections.

### 3.4.1 UAV System Architecture Overview

#### What this section says in simple words

- This section introduces the main physical and logical parts of the system.
- The UAV is the DJI M350 RTK with its camera and sensing payload.
- The Dock is the fixed station that stores, charges, deploys, and communicates with the drone.
- The operator does not control the drone directly.
- Instead, the operator uses FlightHub 2 through a browser.
- FlightHub 2 is hosted on an Azure virtual machine.
- The chapter presents the Dock as a central communication hub between the drone and the cloud.
- That is a key design idea in this chapter.
- The drone collects data and flies the mission.
- The Dock relays and manages communication.
- The cloud hosts coordination and management functions.
- The operator interacts with the system through the cloud interface.
- The student also explains why this hardware set was selected.
- The DJI platform is presented as enterprise-grade and suitable for public safety or emergency response.
- A third-party 5G module is introduced as the way to add 5G support.
- The student then describes the main technical capabilities of the drone and payload, such as endurance, GNSS support, RTK accuracy, cameras, thermal sensing, and weather resistance.
- The section also explains that the Dock communicates with FlightHub 2 through MQTT and with the UAV through DJI's own protocol.
- The operator is intentionally separated from direct drone access.
- This centralizes control through FlightHub 2.

#### What the reader should understand from this section

- The thesis system is not just a drone in the air.
- It is a multi-part control chain.
- The most important chain is: operator -> FlightHub 2 -> Dock -> UAV.
- This means attacks against the browser, cloud, Dock, or network can all affect flight operations.
- The Dock is especially important because it sits between the UAV and the cloud side.

#### Main ideas to keep in mind while reading

- Drone as mission asset.
- Dock as communications and relay point.
- FlightHub 2 as cloud C2 platform.
- Browser as operator entry point.
- No direct operator-to-UAV link.

### 3.4.2 Public 5G Network Architecture for UAV Connectivity

#### What this section says in simple words

- This section explains how public 5G supports UAV connectivity.
- The student describes both the radio side and the core network side.
- On the radio side, the UAV and Dock connect through gNodeBs.
- On the core side, functions such as AMF, SMF, PCF, and UPF manage authentication, session handling, policy, and data forwarding.
- The student emphasizes that the N6 interface is where traffic leaves the operator's 5G domain and reaches the outside network.
- This matters because it marks a change in security responsibility.
- The section also explains why public 5G is attractive: wide-area coverage, high bandwidth, low latency, and support for BVLOS operations.
- Network slicing is introduced as a way to give UAV traffic dedicated resources and better QoS.
- The student is therefore showing that 5G is both an enabler and a dependency.

#### What the reader should understand from this section

- The 5G network is not a background detail.
- It is a central part of the system architecture.
- The UAV mission depends on how the radio and core network handle mobility, session setup, and traffic delivery.
- The N6 point is especially important because after that point, the traffic leaves the mobile operator's protected domain.

#### Main ideas to keep in mind while reading

- gNB for radio access.
- Core functions for session and policy handling.
- N6 as the exit toward external networks.
- Slicing as a performance and isolation assumption.

### 3.4.3 UAV Integration with Azure Cloud

#### What this section says in simple words

- This section explains how the cloud side is built.
- FlightHub 2 is hosted on an Azure VM.
- Azure services provide networking, protection, storage, identity, and monitoring.
- The Dock side connects into Azure through a VPN Gateway.
- The operator side connects through Azure Front Door using a browser over HTTPS.
- Azure Firewall Premium is placed in the path to inspect and control traffic.
- Microsoft's identity platform handles identity and authentication.
- Blob Storage, SQL, Key Vault, Functions, Monitor, and other Azure services support different parts of the platform.
- Azure Communication Services is used for video streaming.
- The section also describes layered protection such as VPN encryption, WAF, TLS, IDPS, and private network controls.
- In simple words, the student is building the cloud side as a layered defended environment around the FlightHub 2 server.

#### What the reader should understand from this section

- Azure is not just hosting the application.
- It provides the security and operations environment around it.
- The cloud architecture is built in layers so that operator traffic, Dock traffic, storage, and management are separated and controlled.
- The operator path and Dock path are different, but both eventually feed into the same central control platform.

#### Main ideas to keep in mind while reading

- Browser path through Front Door.
- Dock path through VPN.
- Firewall as inspection point.
- Cloud identity service for authentication and access control.
- ACS for video delivery.

### 3.5 UAV Communication Data Flow

#### What this section says in simple words

- This part explains how communication happens during the mission lifecycle.
- The chapter first explains how the 5G connection is established.
- Then it explains the mission from login to control loop to video streaming to return-to-home and session termination.
- Finally, it marks the trust boundaries and data flows that later drive the threat model.

### 3.5.1 5G Registration and PDU Session Establishment

#### What this section says in simple words

- The UAV modem and Dock modem both act like 5G user equipment.
- They scan for the strongest gNB and start the registration process.
- The AMF handles the registration flow and coordinates with other core functions.
- The system authenticates the device, retrieves slice and QoS information, and assigns identifiers.
- Then a PDU session is created so the device can communicate with the Azure cloud.
- The SMF, PCF, and UPF coordinate policy, traffic handling, and tunnel setup.
- The section also explains that a dedicated network slice can be used to guarantee better performance for emergency missions.
- The overall meaning is that before any mission data can move, the 5G side must first create a working session and route.

#### What the reader should understand from this section

- Secure and stable UAV communication depends on the 5G registration and session process.
- If this process is weak or disrupted, the rest of the mission cannot function properly.
- This section also helps explain why network policy and slice assumptions matter later.

### 3.5.2 The UAV System End-to-End Operation Data Flow

#### What this section says in simple words

- This is the operational heart of the chapter.
- The student breaks the mission into ten phases.
- Phase 1 is operator login and JWT issuance.
- Phase 2 is creation of MQTT credentials for direct remote control.
- Phase 3 is establishment of the site-to-site VPN between Dock and Azure.
- Phase 4 is the Dock connecting to the MQTT broker and being authorized.
- Phase 5 is mission planning and dispatch.
- The operator creates a mission plan, FlightHub stores it, and the Dock forwards it to the UAV.
- Phase 6 is the real-time control loop.
- Commands go from FlightHub to Dock to UAV, while telemetry goes back from UAV to Dock to FlightHub and then to the browser.
- Phase 7 is live video streaming through Azure Communication Services.
- Phase 8 is mid-mission command injection by the legitimate operator, such as waypoint changes.
- Phase 9 is return-to-home and media offload.
- Phase 10 is session termination and cleanup.
- The most important message here is that all mission activity flows through a defined chain of services and protocols.

#### What the reader should understand from this section

- The thesis is mapping the real operational journey of data and commands.
- Command, telemetry, authentication, video, and mission planning do not all use the same path.
- JWTs, MQTT, VPN, WebSocket, WebRTC, and DPP each play different roles.
- This section is later used to explain where attacks can happen.

#### Main ideas to keep in mind while reading

- Login and token issuance come first.
- Dock-cloud trust is established before command flow.
- Mission control is continuous and stateful.
- Video is handled separately from command and telemetry.
- Cleanup and token invalidation matter after the mission too.

### 3.5.3 Trust Boundaries and Primary Data Flows

#### What this section says in simple words

- This section marks the exact places where trust changes.
- The student identifies seven trust boundaries labeled A to G.
- These boundaries include the UAV-to-Dock wireless path, the Dock-to-5G side, the browser-to-internet side, the internet-to-Azure entry side, and internal Azure transitions.
- The student then lists ten main data flows labeled DF1 to DF10.
- These flows describe which protocol or path is used between source and destination.
- Examples include the drone-to-Dock link, the IPsec tunnel, browser-to-Front Door traffic, Azure internal flows, and service-to-service traffic.
- In simple words, the student is turning the architecture into a security map.
- Every place where data crosses a boundary or moves through a flow can later be analyzed for threats.

#### What the reader should understand from this section

- Trust boundaries are not just diagrams.
- They are the foundation for the later STRIDE analysis.
- If a boundary is exposed, then it becomes a likely attack point.
- If a flow is critical, then integrity, confidentiality, and availability for that flow become very important.

#### Main ideas to keep in mind while reading

- Boundary A and the other radio-related boundaries matter for rogue gNB and jamming concerns.
- Browser-related boundaries matter for token theft and web threats.
- Internal Azure flows matter for cloud compromise and lateral movement.
- The Dock remains central because many flows pass through it.

## Quick recap of Chapter 3

- Chapter 3 defines the exact system studied in the thesis.
- It shows the drone, Dock, public 5G, Azure cloud, FlightHub 2, and browser as one connected architecture.
- It explains how 5G connectivity is established.
- It explains the ten phases of the mission communication lifecycle.
- It ends by marking the trust boundaries and primary data flows that feed directly into the threat model.
- If Chapter 3 is read correctly, the reader should finish it with a clear mental picture of the full UAV-5G-cloud system and where the key security exposures sit.