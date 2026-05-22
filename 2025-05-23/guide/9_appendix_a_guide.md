# Guide: Appendix A - Complete STRIDE Threat Catalog

## What this guide does

This guide explains what Appendix A contains in simple words. It does not repeat all 80 rows, but it tells you what each component block is saying and what kind of threat logic the appendix is documenting.

## Appendix A in one simple view

- Appendix A is the detailed threat inventory behind Chapter 5.
- It lists 80 threats across eight system components.
- Each row tells you the threat ID, STRIDE category, description, plausibility, impact, and related data flow.
- In simple words, this appendix is the structured evidence table proving that the thesis threat model is systematic rather than selective.

## How to read this appendix

- Read it as the detailed source behind the Chapter 5 summary table.
- The appendix is organized by component, not by attack scenario.
- This means you should think of it as a component-by-component threat map of the whole system.

## Detailed reading guide

### UAV block

- The UAV threats focus on attacks directly affecting the aircraft and its immediate control path.
- Spoofing includes rogue base station impersonation, GNSS spoofing, and replay of captured commands.
- Tampering includes command modification and firmware modification.
- Information disclosure covers interception of telemetry or leakage of stored data.
- Denial of service focuses especially on radio jamming and command flooding effects.
- Elevation of privilege includes abuse of low-level interfaces such as the development or companion path.
- In simple words, this block says the drone can be attacked through radio, navigation, firmware, storage, and local technical interfaces.

### Dock block

- The Dock threats focus on its role as relay, storage point, and trust bridge.
- Spoofing includes stolen certificates and redirection of traffic.
- Tampering includes mission-file manipulation and physical interference with Dock behavior.
- Repudiation and information disclosure cover local log and storage exposure.
- Denial of service targets tunnel stability and message handling.
- Elevation of privilege highlights default credentials and local administration weaknesses.
- In simple words, this block says the Dock is a high-value bridge between UAV and cloud, so both identity and local-hardening risks matter heavily.

### Browser block

- The browser threats focus on the operator side.
- Spoofing includes phishing and request-forgery style abuse.
- Tampering includes malicious browser-side changes to payloads or tokens.
- Repudiation captures the problem of proving who issued what command.
- Information disclosure covers token theft and browser-stored mission data leakage.
- Denial of service includes client-side resource exhaustion and access disruption.
- Elevation of privilege includes browser or workstation compromise leading to deeper control abuse.
- In simple words, this block says the operator endpoint is a major security gateway because command authority begins there.

### FlightHub 2 block

- The FlightHub 2 threats focus on the central cloud C2 application.
- Spoofing includes login bypass and forged-token problems.
- Tampering includes mission database manipulation and malicious payload injection through application paths.
- Repudiation highlights insufficient logging of critical actions.
- Information disclosure focuses on mission and telemetry exposure through misconfigured storage.
- Denial of service focuses on API overload and MQTT resource exhaustion.
- Elevation of privilege includes container escape and weak application privilege boundaries.
- In simple words, this block says compromise of the central cloud control platform can have fleet-wide consequences.

### Public 5G network block

- The public 5G threats focus on radio and core-network exposure.
- Spoofing includes rogue base stations and identity-catcher style tracking.
- Tampering includes command modification and malicious control-plane abuse.
- Repudiation and information disclosure cover network records, signaling, and metadata leakage.
- Denial of service includes jamming and session-flood style disruption.
- Elevation of privilege includes compromise of edge or core network functions.
- In simple words, this block says the mobile network is a major attack surface because it sits between the UAV system and infrastructure the operator does not control.

### Front Door and WAF block

- These threats focus on the cloud edge entry point.
- Spoofing includes DNS and header-based trust abuse.
- Tampering includes request smuggling and rule bypass paths.
- Repudiation and information disclosure concern session logging and certificate exposure.
- Denial of service includes volumetric flooding and protocol abuse.
- Elevation of privilege includes policy misconfiguration that opens deeper management access.
- In simple words, this block says the web edge can be attacked both as an availability target and as a trust-bypass point.

### VPN Gateway block

- This block focuses on the secure tunnel path between Dock and Azure.
- Spoofing includes stolen client certificates or redirection of tunnel setup.
- Tampering includes downgrade attempts and route-table abuse.
- Repudiation and information disclosure focus on logging and diagnostic leakage.
- Denial of service includes re-key flooding and endpoint exhaustion.
- Elevation of privilege includes management-plane compromise.
- In simple words, this block says the VPN is not only a protection mechanism; it is also itself a security-critical asset that can be attacked.

### Communication Services block

- This block focuses on the video and room-signaling layer.
- Spoofing includes unauthorized room joins and fake stream injection.
- Tampering includes manipulation of video content.
- Information disclosure includes key-exchange or metadata leakage concerns.
- Denial of service covers signaling floods, forced disconnection, and bandwidth exhaustion.
- Elevation of privilege includes abuse of management APIs or weak room-access policy.
- In simple words, this block says the video service path adds another attack surface separate from the command path.

## What this appendix tells you overall

- The threat catalog is broad because the system is broad.
- Threats exist at the UAV, edge, browser, cloud, network, tunnel, and media-service levels.
- Spoofing, tampering, denial of service, and privilege abuse recur across many components.
- The appendix supports the thesis claim that the UAV-5G-cloud architecture must be analyzed as one integrated system.

## Quick recap

- Appendix A is the detailed threat table behind Chapter 5.
- It maps 80 threats across eight components.
- Each block shows a different part of the architecture's attack surface.
- If Appendix A is read correctly, the reader should understand how the thesis turns the full system architecture into a structured threat inventory with component-level traceability.