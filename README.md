# Awesome-Zero-Trust-Security-Assessment

## Top Zero Trust Security Assessment Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Zero Trust Posture Scoring, Tenant Configuration Audits & Self-Hosted Identity Auditing*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Zero Trust Security Assessment**. These tools enable organizations to measure how closely their identity, device, network, and data controls align with Zero Trust principles—surfacing misconfigurations, quantifying risk, and prioritizing remediation before attackers exploit trust gaps.



**Examples** include CrowdStrike Falcon Zero Trust Assessment, Microsoft Zero Trust Assessment, Zscaler Zero Trust Exchange, Palo Alto Zero Trust Posture Center, Cisco Zero Trust Assessment, Illumio Zero Trust, BeyondTrust Zero Trust, Duo Zero Trust, CyberArk Zero Trust, and Akamai Zero Trust (the category leaders).



**Open-source emphasis**: Zero Trust Assessment is a domain where open-source tooling is **narrow but genuinely useful for identity and tenant auditing**. The strongest active project is **Microsoft's ZeroTrustAssessment**—a fully open-source PowerShell module (MIT, 2,000+ GitHub stars) that tests hundreds of configuration items across Microsoft 365 and Azure against Zero Trust best practices, stores all data locally, and generates a detailed HTML report with remediation steps . **iam_audit** provides a focused identity audit mapped to NIST SP 800-53 and the CISA Zero Trust Maturity Model Identity pillar, with MFA coverage measurement and over-privileged account detection . **Octelium** and **Aegis** are not assessment tools but *enforcement* platforms—they implement Zero Trust access control rather than measure it . The critical gap: **no open-source tool provides a unified, cross-vendor assessment** covering network segmentation, workload identity, and data access posture comparable to Palo Alto's Zero Trust Posture Center or CrowdStrike Falcon ZTA.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[CrowdStrike Falcon Zero Trust Assessment](https://www.crowdstrike.com/)**  

  Real-time endpoint security and compliance scoring within Falcon Insight; evaluates over 120 endpoint settings (sensor health, applied policies, OS security) and produces an overall score shareable with Zero Trust ecosystem partners for conditional access enforcement . Supports Windows, macOS, and Linux, with API access for integration into access decisions .



- **[Microsoft Zero Trust Assessment](https://learn.microsoft.com/en-us/security/zero-trust/assessment/overview)**  

  Open-source PowerShell tool (see open-source section) that also anchors Microsoft's assessment offering; tests hundreds of configuration items across Microsoft 365 and Azure aligned with the Secure Future Initiative and Zero Trust pillars, with remediation guidance in an interactive HTML report .



- **[Zscaler Zero Trust Exchange](https://www.zscaler.com/)**  

  Cloud-native Zero Trust platform with inline inspection (ZIA), private application access (ZPA), and continuous posture validation; provides telemetry and Risk360 insights to identify control gaps and misconfigurations across cloud and SaaS environments, though formal compliance ownership remains entity-owned . FedRAMP High and StateRAMP authorized for public sector use .



- **[Palo Alto Networks Zero Trust Posture Center](https://www.paloaltonetworks.com/)**  

  Unified workspace within Strata Cloud Manager that maps NGFW and Prisma Access deployments to Zero Trust 2.0 principles across five dimensions (network configuration, identity, least privilege, inspection, data control); delivers prioritized recommendations with real-time impact analysis and executive reporting with industry comparison .



- **[Cisco Zero Trust Assessment](https://duo.com/solutions/zero-trust-security)**  

  Duo-driven assessment and enforcement suite covering user trust (phishing-resistant MFA), device trust (posture checks), application access (ZTNA), contextual access (risk-based authentication), and continuous verification; SE Labs independent testing confirmed detection of 30 identity-based attacks . SASE readiness assessments available through partners .



- **[Illumio Zero Trust](https://www.illumio.com/)**  

  Segmentation-first Zero Trust platform that maps every workload connection in real time and auto-generates policy from observed traffic; enforces least privilege between applications across cloud, containers, endpoints, and data centers without IP-based rules . Assessment is implicit in the visibility-to-policy workflow rather than a separate scoring report.



- **[BeyondTrust Zero Trust](https://www.beyondtrust.com/)**  

  Privileged Access Management (PAM) as a foundational Zero Trust control; enforces least privilege, removes local admin rights, isolates privileged sessions, and provides audit trails aligned with NIST's seven Zero Trust tenets and CISA guidance . FedRAMP authorized for government use.



- **[Duo Zero Trust](https://duo.com/)**  

  Cisco's identity-focused Zero Trust solution covering MFA, device trust, adaptive access policies, and continuous session verification; provides a five-phase implementation framework (establish user trust, verify device trust, enable access, enforce contextual access, verify continuously) .



- **[CyberArk Zero Trust](https://www.cyberark.com/)**  

  Identity security platform integrating with Palo Alto Networks and CrowdStrike to enforce identity-driven Zero Trust access; protects credentials, secrets, and privileged sessions, with integrations that block out-of-compliance endpoints from connecting to IT resources based on Falcon ZTA scores .



- **[Akamai Zero Trust](https://www.akamai.com/)**  

  Microsegmentation, ZTNA, and FIDO2-compliant MFA for defense and government agencies; emphasizes agentless east-west traffic visibility, private CDN isolation, and API security aligned with the Zero Trust Reference Architecture 2.0 and Executive Order 14028 . FedRAMP authorized.



## Open-Source GitHub Projects



### Tenant & Identity Assessment Tools



- **[Microsoft ZeroTrustAssessment](https://github.com/microsoft/zerotrustassessment)**  

  The most comprehensive open-source **Zero Trust tenant assessment** available (MIT, PowerShell 7) . Connects to Microsoft Graph, Azure, Exchange, SharePoint, and Azure Information Protection to test **hundreds of configuration items** against Microsoft's best practices, industry standards (NIST, CISA, CIS), and internal security baselines . Read-only operation with **all data stored locally**—no cloud exfiltration. Generates an interactive HTML report organized by Zero Trust pillar (Identity, Devices, Network, Data) with risk ratings and remediation steps . Requires Global Administrator consent on first run (subsequent runs can use Global Reader) . **The strongest starting point for Microsoft 365/Azure environments**—but it is Microsoft-specific and does not assess third-party security tools.



- **[iam_audit](https://zenodo.org/records/23167740)**  

  Open-source **Zero Trust identity and access audit** for small and mid-sized organizations (v0.1.0, October 2026) . Features **13 identity checks** mapped to 11 NIST SP 800-53 Rev. 5 controls and indicative CISA Zero Trust Maturity Model stages for Authentication, Identity Stores, and Access Management; measures MFA coverage and phishing-resistant MFA; detects orphaned, inactive, never-used, shared, and over-privileged accounts; outputs HTML, Markdown, CSV, and JSON reports via CLI and Streamlit dashboard . **The most focused open-source identity audit** aligned to CISA ZTMM—but it covers identity only, not device/network/data pillars.



### Enforcement Platforms (Zero Trust Implementation, Not Assessment)



- **[Octelium](https://github.com/octelium/octelium)**  

  Fully open-source, self-hosted **Zero Trust access platform** built on identity-aware proxies and Kubernetes . Features dynamic secretless access (HTTP APIs, SSH, Kubernetes, databases without sharing credentials), fine-grained ABAC policy-as-code (CEL/OPA), continuous strong authentication (FIDO2/WebAuthn, TOTP, TPM), and OpenTelemetry-native audit logging. **Not an assessment tool**—it implements Zero Trust enforcement, which can be *evaluated* for posture but does not generate assessment reports itself.



- **[Aegis](https://github.com/pushkar-gr/Aegis)**  

  Open-source **identity-based microsegmentation firewall** using eBPF/XDP (Go control plane, Rust data plane) . Default-drop posture that dynamically opens network paths only after user authentication; automatically revokes rules after 60 seconds of inactivity. **Enforcement-focused**—useful for implementing Zero Trust network controls, not for assessing existing posture.



### Additional Strong Open-Source Options



- **CyberDudeBivash Zero-Trust Network Access Validator Scanner** — Open-source ZTNA policy scanner supporting Cloudflare Zero Trust, Zscaler Private Access, Palo Alto Prisma Access, Microsoft Entra Conditional Access, and Fortinet ZTNA; detects misconfigurations, simulates breach paths, and generates remediation playbooks . **Early-stage** (single maintainer, paid Pro tier) but covers multi-vendor ZTNA policy auditing—a gap not filled by Microsoft's tool.

- **eBPF Microsegmentation** — Open-source kernel-native microsegmentation for cloud-native environments (Go agent/server, React UI); enforces network isolation at line rate . **Enforcement tool** rather than assessment—useful for implementing Zero Trust network controls.



**Frameworks for building custom systems**: For **Microsoft 365/Azure tenants**, Microsoft ZeroTrustAssessment provides the most thorough automated audit with local-only data handling . For **identity-focused audits** aligned to CISA ZTMM, iam_audit covers MFA coverage and account hygiene . For **multi-vendor ZTNA policy validation**, the CyberDudeBivash scanner offers early-stage coverage . No open-source tool matches the cross-pillar, cross-vendor posture scoring of Palo Alto's Zero Trust Posture Center or CrowdStrike Falcon ZTA—organizations requiring unified assessment across network, endpoint, and identity should evaluate commercial platforms.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Zero Trust assessment tools handling tenant configuration and security posture data must comply with organizational security policies; **assessment reports contain sensitive architecture information** and should be stored and shared only with authorized personnel .

- **Open-source Zero Trust assessment is strongest for Microsoft tenants and identity auditing**—Microsoft ZeroTrustAssessment and iam_audit provide production-grade, local-only evaluation . However, **no open-source tool provides unified cross-vendor posture scoring** across endpoint, network, and data pillars. Organizations requiring comprehensive Zero Trust assessment should evaluate commercial platforms like Palo Alto Posture Center or CrowdStrike Falcon ZTA.

- Verify license terms for commercial use; Microsoft ZeroTrustAssessment is MIT-licensed , and iam_audit is open-source (check Zenodo record).



---



**Made for security architects, Zero Trust program leads, identity engineers, and compliance teams.**  

Let's make Zero Trust assessment more open, but with clear eyes about the cross-vendor posture gap that commercial platforms still fill.
