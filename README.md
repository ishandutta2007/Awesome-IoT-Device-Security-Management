# Awesome-IoT-Device-Security-Management

# Top IoT Device Security Management Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Device Discovery, Vulnerability Management & Self-Hosted IoT Security Platforms*  
**Last updated: October 2026**

This repository tracks notable **commercial IoT security platforms** and **open-source projects** that discover, monitor, and protect connected devices — from agentless network visibility to firmware analysis and automated threat response.

**Examples** include AWS IoT Device Defender, Armis, Claroty, Microsoft Defender for IoT, Forescout, Sternum, Karamba Security, Vdoo, Finite State, and Nozomi Networks (the category leaders).

**Open-source emphasis**: IoT device security management is a growing open-source domain. **Quantum IoT Security** brings production-grade post-quantum cryptography, anomaly detection, and firmware analysis into a single platform . **mithril** delivers offline firmware content analysis for secrets, SBOM, CVEs, and boot-security posture . **Argus** provides LoRaWAN network security monitoring with packet flooding, replay attack, and RF jamming detection . **MUD-PD** from NIST automates device behavior characterization and MUD file generation . **MUDIS** compares and generalizes MUD profiles across firmware versions . **Magistrala** offers a cloud-native IoT platform with fine-grained access control and mTLS provisioning . This section is heavily expanded.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Armis Centrix](https://www.armis.com/)**  
  **Agentless IoT/OT security platform** — continuous monitoring and strict access controls for connected devices . **Nvidia cybersecurity AI integration** for critical infrastructure protection without performance impact . **Zero Trust security solutions tailored for OT environments** . **Best for agentless asset discovery and Zero Trust** .

- **[Claroty](https://www.claroty.com/)**  
  **Cyber-physical systems protection platform** — visibility solutions for industrial control systems and OT environments . **Threat detection, secure access, and exposure management** capabilities . **Partnerships with Fortinet, Palo Alto, and Siemens** for firewall integrations . **Best for industrial IoT and OT security** .

- **[Nozomi Networks](https://www.nozominetworks.com/)**  
  **Real-time visibility and cybersecurity for ICS and critical infrastructure** . **Combines network and endpoint visibility with threat detection and AI-powered analysis** . **Strategic investors include Mitsubishi Electric, Schneider Electric, Honeywell, and Johnson Controls** . **Best for critical infrastructure protection** .

- **[Forescout](https://www.forescout.com/)**  
  **Pervasive network security** — continuous monitoring and access control of endpoints, network users, and applications . **Automated security controls** to discover, assess, and govern compliance of IT, OT, IoT, and IoMT assets . **Best for heterogeneous network visibility** .

- **[Finite State](https://www.finitestate.io/)**  
  **Software risk management for connected devices** — firmware analysis and software supply chain security . **Acquired MergeBase** to protect every aspect of the software development lifecycle . **Best for connected device risk management** .

- **[AWS IoT Device Defender](https://aws.amazon.com/iot-device-defender/)**  
  **AWS's managed IoT security service** — audit, detect, and mitigate security issues across IoT fleets . **Best for AWS-native IoT security** .

- **[Microsoft Defender for IoT](https://azure.microsoft.com/en-us/products/defender-for-iot/)**  
  **Microsoft's IoT/OT security platform** — agentless network monitoring and threat detection . **Best for Azure-native IoT security** .

- **[Sternum](https://www.sternum.io/)**  
  **IoT security platform** — on-device monitoring and protection for connected devices.

- **[Karamba Security](https://www.karamba.com/)**  
  **Automotive and IoT cybersecurity** — on-device runtime protection.

- **[Vdoo](https://www.vdoo.com/)**  
  **IoT security and certification platform** — automated device security analysis (acquired by JFrog).

## Open-Source GitHub Projects

### IoT Security Platforms

- **[Quantum IoT Security](https://github.com/garrv105/quantum-iot-security)**  
  **Production-grade platform combining post-quantum cryptography with real-time IoT threat detection and automated incident response** . **IoT device fingerprinting** via behavioral identification of protocol, port, and timing analysis with automatic classification (sensor, camera, gateway, actuator, controller) . **Anomaly detection** using lightweight Isolation Forest and Local Outlier Factor models designed for resource-constrained environments . **Post-quantum cryptography** with lattice-based (Kyber-like) key exchange, AES-256-GCM secure channels, and X.509 certificate management . **Incident response automation** with threat-level-based policies, device quarantine, alerting, and traffic blocking . **Firmware analysis** with static analysis, entropy computation, string extraction, CVE matching, and CVSS scoring . **Compliance reporting** mapping to NIST IoT Cybersecurity framework and IEC 62443 . **FastAPI server with CLI and Docker deployment** . **Best for production IoT security with post-quantum cryptography** .

- **[Argus](https://github.com/mgs042/Argus)**  
  **IoT network security monitoring and resource management tool for LoRaWAN networks** . **Integrates with Chirpstack Application Server** — collects event metrics and monitors network resources . **Threat detection** for packet flooding, join request replay, frame count reset/device reset, packet loss, active/inactive devices and gateways, RF jamming (RSSI and SNR threshold breach), link margin threshold breach, battery status, and gateway location shift . **Stores metrics in InfluxDB** with downsampling via predefined Influx Tasks . **Celery workers for background threat detection** and metric processing . **Docker Compose deployment** with scalable Celery workers based on network traffic . **Telegram alert integration** available . **Best for LoRaWAN network security monitoring** .

- **[Magistrala](https://github.com/absmach/magistrala)**  
  **Modern, Go-based, cloud-native IoT platform framework** (formerly Mainflux), Apache-2.0 licensed . **Fine-grained access control** — define object-scoped roles like "reader on channel1" . **Atom integration model** provides identity, authorization, and catalog with workspaces, entities, resources, and groups . **Provision utility** creates channels and clients with certificate generation for mTLS use cases . **Scales from simple prototypes to complex deployments** without rigid patterns . **Best for high-performance, cloud-native IoT core with security** .

### Firmware Analysis & SBOM Tools

- **[mithril](https://github.com/nmatt0/mithril)**  
  **IoT static scanner for firmware content analysis — secrets, SBOM, CVEs, licenses, and boot-security posture** . **Analyzes firmware contents** whether a single file or unpacked rootfs . **Firmware-aware SBOM** recovers components from package databases (dpkg/opkg/apk/rpm), ELF version banners, versioned libc filenames, and kernel banner — finds openssl/busybox/uClibc even in stripped images without package managers . **Emitted as CycloneDX and SPDX** . **Offline CVE analysis** with local OSV + NVD/CPE mirror, curated kernel-CVE checklist, CISA KEV and EPSS annotation . **Secrets detection** with deterministic offline ladder: pattern → structural → validated . **Weak and leaked key detection** — checks if private half is obtainable via fingerprint match against known compromised keys (rapid7 ssh-badkeys, Vagrant insecure key), ROCA fingerprint (CVE-2017-15361), undersized RSA, and factoring recoveries . **Fully offline and reproducible** — no network at scan time . **Safe on hostile input** with bounds-checked reader and clean error degradation . **Submitted for inclusion in Kali Linux** (Debian package ready) . **Best for firmware security auditing and supply chain analysis** .

- **[UniBOM](https://ora.ox.ac.uk/objects/uuid:003eb0e1-5e6c-404e-b484-33358e8d7bb7)**  
  **Advanced SBOM generation, analysis, and visualisation tool for IoT systems** — integrates binary, filesystem, and source code analysis . **Fine-grained vulnerability detection** with support for non-package-managed C/C++ dependencies . **Historical CPE tracking, AI-based vulnerability classification** by severity and memory safety . **Addresses memory-related vulnerabilities** that account for over 70% of known IoT security threats . **Demonstrated superior detection** through comparative analysis of 258 wireless router firmware binaries . **Web GUI for visualising SBOM analysis** with interactive dashboards, trend analysis, and risk visualisation . **Packaged for open-source distribution** . **Best for comprehensive SBOM-driven IoT security management** .

### MUD (Manufacturer Usage Description) Tools

- **[MUD-PD](https://www.nist.gov/news-events/news/2025/08/final-nist-ir-8349-released-characterize-secure-your-iot-devices)**  
  **NIST's open-source tool for automating IoT device behavior characterization and MUD file generation** . **Supports NIST IR 8349 methodology** for capturing, documenting, and characterizing the entire range of an IoT device's network behavior across use cases and conditions . **Enables manufacturers, network operators, and researchers to generate MUD files** — standard specification of network communications an IoT device requires . **Best for automated device behavior characterization** .

- **[MUDgee](https://github.com/ayyoob/mudgee)**  
  **Automated MUD profile generation from network traffic traces**, open-source . **Generates MUD profiles from runtime network traffic** for device identification and behavioral analysis . **Used for verifying and monitoring IoT network behavior** . **Best for MUD profile generation from traffic** .

- **[MUDIS](https://deepness-lab.org/wp-content/uploads/2022/03/222052.pdf)**  
  **MUD Inspection System — web application for analyzing and comparing MUD files**, open-source with Docker setup . **Comparison task visualizes differences** between two MUD files with similarity score (Jaccard coefficient), highlighting identical, similar, clustered, and dissimilar ACEs . **Generalization task outputs unified MUD** that white-lists network behavior of both inputs using domain ranges (e.g., `*.iotvendor.com`) for fewer, more explainable rules . **Useful for analyzing MUDs from different traffic conditions, comparing firmware versions, identifying anomalies, and spotting malware-infected devices** . **Best for MUD analysis and comparison** .

### Additional Strong Open-Source Options

- **IoT Sentinel** — Automated device-type identification for security enforcement, based on 2017 IEEE ICDCS paper, implementation forked and updated for evaluation  .
- **IoTDevID** — Behavior-based device identification method, original code available from Kahraman Kostas (consolidated into evalIoT codebase)  .
- **GenIoTID** — Implementation of generalizable feature set and ML algorithm for IoT device identification from NDSS 2025 paper  .
- **Runtime MUD identification** — Runtime device identification using MUD profiles  .
- **Mongoose OS** — IoT firmware development framework with OTA, flash encryption, crypto chip support, and built-in AWS IoT/Google/Azure integration, Apache 2.0 Community Edition  .
- **MUDIS** — MUD inspection and comparison web application  .

**Frameworks for building custom IoT device security management solutions**: Combine **Quantum IoT Security** for post-quantum cryptography, device fingerprinting, anomaly detection, and automated incident response . Use **mithril** for offline firmware content analysis — secrets, SBOM, CVEs, licenses, and weak key detection . Deploy **Argus** for LoRaWAN network security monitoring with threat detection for packet flooding, replay attacks, and RF jamming . Integrate **MUD-PD** and **MUDgee** for automated device behavior characterization and MUD profile generation . Use **MUDIS** for comparing and generalizing MUD profiles across firmware versions . Deploy **Magistrala** for cloud-native IoT platform with fine-grained access control and mTLS . Note that true enterprise IoT security management with managed infrastructure, global scale, and vendor-supported SLAs (Armis, Claroty, Nozomi Networks) remains primarily commercial territory; open-source stacks provide strong firmware analysis, MUD tooling, and anomaly detection foundations that require integration for complete IoT security management.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- IoT device security platforms handle sensitive device credentials and network traffic. Self-hosted solutions require proper security hardening, access controls, and compliance with data privacy regulations.
- **Firmware analysis requires unpacking** — mithril analyzes unpacked rootfs; pair with moria for identify/unpack step (`moria -e firmware.bin`, then `mithril firmware.bin.extracted/`) .
- **Post-quantum cryptography is emerging** — Quantum IoT Security implements lattice-based key exchange, but PQC standards are still evolving .
- **MUD is a formal IETF specification** — MUD files capture device run-time behavior and are amenable to rigorous automated evaluation and anomalous behavior detection .
- **License considerations**: Quantum IoT Security is open-source , mithril is MIT , Argus is open-source , Magistrala is Apache-2.0 , and Mongoose OS Community Edition is Apache 2.0 . Verify licensing against your use case before committing.
- The open-source ecosystem provides strong firmware analysis, MUD tooling, and anomaly detection foundations, but **managed infrastructure, global scale, and vendor-supported SLAs** remain primarily commercial offerings.

---

**Made for IoT security engineers, embedded developers, and organizations seeking IoT device security sovereignty.**
Let's make IoT device security management more open, transparent, and secure.
