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

| Product | Description | Starting Pricing | Free Tier / Free Trial Limits |
| :--- | :--- | :--- | :--- |
| **[CrowdStrike Falcon Zero Trust Assessment](https://www.crowdstrike.com/)** | Real-time endpoint security and compliance scoring within Falcon Insight; evaluates over 120 endpoint settings (sensor health, applied policies, OS security) and produces an overall score shareable with Zero Trust ecosystem partners for conditional access enforcement. Supports Windows, macOS, and Linux with API access. | **$59.99/device/year** (Falcon Go tier; enterprise packages typically ~$90–$180/device/year) | **15-day free trial**; covers up to 100 devices (includes Falcon Prevent NGAV and USB Device Control). |
| **[Microsoft Zero Trust Assessment](https://learn.microsoft.com/en-us/security/zero-trust/assessment/overview)** | Automated tenant posture tool testing hundreds of configuration items across Microsoft 365 and Azure against Zero Trust pillars, with remediation guidance in an interactive HTML dashboard. | **Free / $0** (Open-source assessment engine requiring only existing M365/Azure tenant credentials; Entra ID P1/P2 remediation licenses start at $6/user/month) | **Free forever**; unlimited tenant evaluation runs and configuration checks (no user limits on the assessment tool itself). |
| **[Zscaler Zero Trust Exchange](https://www.zscaler.com/)** | Cloud-native Zero Trust platform with inline inspection (ZIA), private application access (ZPA), and continuous posture validation; provides Risk360 telemetry to identify control gaps across cloud and SaaS environments. FedRAMP High and StateRAMP authorized. | **$72/user/year** (~$6/user/month for entry standalone ZIA/ZPA; combined bundles start at ~$250–$280/user/year) | **30-day proof of concept (PoC)**; evaluation access provisioned through sales engineering for scoped enterprise pilot environments. |
| **[Palo Alto Networks Zero Trust Posture Center](https://www.paloaltonetworks.com/)** | Unified workspace within Strata Cloud Manager mapping NGFW and Prisma Access deployments across five dimensions (network configuration, identity, least privilege, inspection, data control); delivers prioritized recommendations and real-time impact analysis. | **$110/user/year** (Prisma Access Mobile User Business tier; Strata Cloud Manager Pro add-on priced at ~30% of NGFW estate value) | **30-day guided evaluation / PoC**; evaluation licenses coordinated via sales/reseller console (Prisma Cloud offers instant 30-day self-service trial). |
| **[Cisco Zero Trust Assessment](https://duo.com/solutions/zero-trust-security)** | Identity-driven assessment and enforcement suite covering phishing-resistant MFA, posture checks, continuous verification, and SASE readiness; validated detection of 30 identity-based attacks in independent SE Labs testing. | **$3/user/month** (Duo Essentials, billed annually; Cisco Secure Access enterprise SSE packages start at ~$15–$25/user/month) | **30-day free trial** (Duo paid plans) or **Duo Free plan** (permanently free up to **10 users** with unlimited app integrations). |
| **[Illumio Zero Trust](https://www.illumio.com/)** | Segmentation-first Zero Trust platform mapping workload connections in real time and auto-generating least-privilege policy across cloud, containers, endpoints, and data centers. | **$30/workload/year** (typical entry pricing for <1,000 workloads; enterprise minimum contracts typically start at $25,000/year) | **14-day free trial** (Illumio Insights); expires if no cloud flow logs are ingested within the first 7 days, with 30-day data retention. |
| **[BeyondTrust Zero Trust](https://www.beyondtrust.com/)** | Privileged Access Management (PAM) enforcing least privilege, removing local admin rights, isolating privileged sessions, and auditing activity against NIST/CISA Zero Trust tenets. FedRAMP authorized. | **$40/endpoint/year** (BeyondTrust Endpoint Privilege Management entry tier, typically under 1,000–asset contracts) | **14-day free trial** (Privileged Remote Access / Remote Support); Endpoint Privilege Management provided via guided enterprise PoC. |
| **[Duo Zero Trust](https://duo.com/)** | Cisco's identity-focused Zero Trust solution covering MFA, device trust, adaptive access policies, and continuous session verification across a five-phase implementation framework. | **$3/user/month** (Duo Essentials tier; Duo Advantage is $6/user/month, Duo Premier is $9/user/month) | **Free forever for up to 10 users** (Duo Free plan: MFA, Duo Mobile push, unlimited application integrations; no device trust or SSO). |
| **[CyberArk Zero Trust](https://www.cyberark.com/)** | Identity security platform integrating with Palo Alto Networks and CrowdStrike to enforce identity-driven Zero Trust access; protects credentials, secrets, and privileged sessions, blocking out-of-compliance endpoints. | **$2/user/month** (CyberArk Identity Workforce SSO/MFA tier; CyberArk Privilege Cloud PAM starts at ~$2,400/privileged user/year) | **14-day free trial** (CyberArk Identity sandbox / virtual training tenant; enterprise PAM evaluated via structured vendor PoC). |
| **[Akamai Zero Trust](https://www.akamai.com/)** | Microsegmentation (Guardicore), ZTNA (Enterprise Application Access), and FIDO2-compliant MFA; emphasizes agentless east-west traffic visibility and API security aligned with Executive Order 14028. FedRAMP authorized. | **$10/user/month** (~$120/user/year for Enterprise Application Access ZTNA; Guardicore priced per workload/server) | **60-day free trial** (Enterprise Application Access ZTNA trial provisioned via partner/sales onboarding request). |

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
