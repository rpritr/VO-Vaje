# Security Improvement Plan
**GreenFields Food Processing Ltd.**

---

## 1. Security Maturity Assessment

GreenFields currently operates at a **low cybersecurity maturity level**, roughly **Level 0–1 (non-existent to ad hoc)** across most security domains. The organization has grown its digital dependence, but its security controls have not matured accordingly. The case shows no formal risk assessment, no security policies, no security monitoring, no incident response plan, inconsistent patching, shared administrator passwords, and no employee security training. In addition, the production network is directly connected to the same LAN as the corporate environment, and backups are stored on the same network.

This creates a high-risk environment where a single phishing attack, stolen credential, or compromised laptop could spread across both office and production systems. The recent incidents in the case confirm that the threat is not theoretical: a phishing attack already succeeded, a laptop with internal documents was lost, and a supplier experienced ransomware.

A brief maturity view:

| Security Domain | Current Level | Target (12–18 months) | Main Gap |
|---|---:|---:|---|
| Risk management | 0 | 2 | No risk assessment or risk register |
| Policies and governance | 0 | 2 | No security policies |
| Access control | 1 | 3 | Shared admin passwords, no MFA |
| Network security | 0 | 2 | No segmentation between corporate and production |
| Endpoint protection | 1 | 2 | Inconsistent patching, limited protection |
| Backup and recovery | 1 | 3 | Backups on same network, no resilient design |
| Incident response | 0 | 2 | No IR plan or playbooks |
| Training and awareness | 0 | 2 | No employee training |
| Monitoring and logging | 0 | 2 | No monitoring or alerting |

Overall, GreenFields is best described as **reactive rather than managed**. Immediate baseline controls are needed before more advanced improvements are attempted.

## 2. Top 10 Security Risks

The following are the most significant cybersecurity risks facing GreenFields.

| # | Risk | Description |
|---|---|---|
| 1 | Ransomware affecting ERP and production systems | A ransomware infection could encrypt systems used for production, logistics, documents, and operations, causing major downtime. |
| 2 | Lateral movement from corporate to production network | Because production is connected directly to the corporate LAN, compromise of a user device could spread into plant systems. |
| 3 | Backup failure during an incident | Backups stored on the same network may be encrypted or deleted during a ransomware event. |
| 4 | Phishing-based credential compromise | An employee already entered credentials into a fake website, showing high susceptibility to account takeover. |
| 5 | Shared administrator password abuse | Shared admin accounts create a high-impact risk because a single compromise could affect all major systems. |
| 6 | Exploitation of unpatched systems | Inconsistent patching across servers, laptops, industrial PCs, and scanners leaves known vulnerabilities exposed. |
| 7 | Lost or stolen device exposing data | A laptop with internal documents was already lost during travel, showing risk of confidential information leakage. |
| 8 | Delayed detection of attacks | With no monitoring, intrusions may continue for days or weeks before being identified. |
| 9 | Ineffective incident handling | Without an incident response plan, containment and recovery would be slow and chaotic. |
| 10 | Governance and compliance failure | No formal security governance means recurring weaknesses remain unmanaged and potentially non-compliant. |

## 3. Priority Security Improvements

The following 10 improvements are designed to deliver the highest reduction in risk while remaining realistic for a company with only a 3-person IT team and an annual security budget of €80,000.

### 1. Implement network segmentation
Separate **corporate**, **production**, **server**, and **guest Wi-Fi** environments using VLANs and firewall rules.

**Why it matters:**  
This is one of the most important controls because it limits the blast radius of a compromise. It reduces the chance that malware or a compromised laptop can spread directly into production systems.

### 2. Enforce MFA on all critical systems
Enable multi-factor authentication for Microsoft 365, VPN, privileged accounts, and any critical business platforms.

**Why it matters:**  
Phishing already succeeded once. MFA significantly reduces the effectiveness of stolen credentials.

### 3. Eliminate shared administrator passwords
Create named administrative accounts, enforce least privilege, and require separate privileged accounts for admin work.

**Why it matters:**  
This improves accountability, reduces abuse risk, and prevents one stolen shared password from becoming a full-environment compromise.

### 4. Improve backup resilience
Adopt a **3-2-1 backup model** with at least one **offline or immutable copy**, and use separate credentials for backup administration.

**Why it matters:**  
The current backup design is too exposed to ransomware. Recovery capability is critical for business continuity.

### 5. Deploy endpoint detection and response (EDR)
Implement centrally managed endpoint protection on laptops, industrial PCs, and critical servers.

**Why it matters:**  
EDR improves malware detection, supports rapid containment, and helps a small IT team respond faster.

### 6. Establish structured patch management
Create a monthly patch cycle, prioritize critical patches within 7–14 days, and use maintenance windows for production systems.

**Why it matters:**  
Unpatched systems are a common attack path. Better patch governance lowers exposure to known vulnerabilities.

### 7. Create a basic security policy set
Develop core policies for access control, passwords/MFA, backup, incident response, acceptable use, remote access, and vendor security.

**Why it matters:**  
Policies provide the governance foundation for consistent security behavior and management oversight.

### 8. Develop an incident response plan
Define incident roles, escalation paths, communication procedures, and playbooks for phishing, ransomware, lost devices, and data breaches.

**Why it matters:**  
Without a plan, response is improvised and costly. A basic IR capability reduces downtime and confusion.

### 9. Launch employee security awareness training
Deliver annual awareness training plus quarterly phishing simulations and reminders.

**Why it matters:**  
People are currently an exposed control gap. Training reduces phishing risk and improves incident reporting.

### 10. Introduce baseline monitoring and alerting
Enable Microsoft 365 audit logging, endpoint alerts, VPN logs, and a lightweight managed monitoring service or MDR provider.

**Why it matters:**  
The organization currently has no detection capability. Monitoring shortens the time between compromise and containment.

## 4. Implementation Roadmap (12–18 Months)

A phased roadmap is recommended so the company can reduce risk quickly without overwhelming the IT team or disrupting production.

### Phase 1 — Immediate Improvements (Months 1–4)
Focus on high-impact, low-disruption controls.

- Perform the first formal risk assessment
- Assign a security owner and management sponsor
- Draft and approve core security policies
- Remove shared administrator passwords
- Enable MFA on Microsoft 365, VPN, and admin accounts
- Improve backup design and create an offsite/immutable copy
- Launch security awareness training
- Begin regular restore testing

**Outcome:** credential risks are reduced, governance begins to mature, and recovery readiness improves.

### Phase 2 — Medium-Term Improvements (Months 5–10)
Focus on technical hardening and attack path reduction.

- Implement network segmentation
- Deploy EDR across endpoints
- Formalize patch management processes
- Enable disk encryption and remote wipe on laptops/mobile devices
- Improve email protection and alerting
- Start regular access reviews

**Outcome:** ransomware spread risk decreases, endpoint security improves, and baseline control maturity rises.

### Phase 3 — Strategic Improvements (Months 11–18)
Focus on resilience, repeatability, and sustained governance.

- Finalize incident response plan and run tabletop exercises
- Introduce lightweight monitoring/MDR
- Review supplier and vendor security dependencies
- Create quarterly security KPI reporting to management
- Conduct annual security review and roadmap refresh

**Outcome:** GreenFields moves from ad hoc security toward a managed baseline program.

## 5. Estimated Budget Allocation (€80,000/year)

The budget should prioritize controls that reduce the most severe risks first.

| Budget Category | Estimated Annual Cost | Purpose |
|---|---:|---|
| Identity and access security | €10,000 | MFA rollout, password manager, privileged account improvements |
| Endpoint protection / EDR | €16,000 | Managed EDR for laptops, industrial PCs, and key servers |
| Network segmentation and firewall improvements | €18,000 | VLAN design, switch/firewall configuration, segmentation support |
| Backup resilience and recovery testing | €12,000 | Offsite/immutable backup capability and monthly restore testing |
| Security awareness training | €5,000 | Training content, phishing simulations, staff awareness program |
| Monitoring / MDR support | €10,000 | Basic managed detection and alert triage |
| External consulting and incident response planning | €7,000 | Risk assessment, policy development, IR playbooks, tabletop exercise |
| Contingency reserve | €2,000 | Minor unplanned costs or urgent gaps |

**Total:** **€80,000**

This allocation is realistic for a medium-sized company with a small internal IT team, because it combines internal execution with selective use of external expertise.

## 6. Metrics for Measuring Security Improvement

Management should track a small set of measurable KPIs that are easy to report and directly tied to business risk.

### 1. Phishing click rate
Percentage of employees who click simulated phishing links.

**Why useful:** measures employee awareness and behavioral improvement.  
**Target:** below 10% within 12 months.

### 2. MFA coverage
Percentage of users and privileged accounts protected by MFA.

**Why useful:** measures reduction in credential-compromise risk.  
**Target:** 100% for admins and VPN, above 95% overall.

### 3. Patch compliance rate
Percentage of systems patched within the defined timeframe.

**Why useful:** measures exposure to known vulnerabilities.  
**Target:** above 90% within 30 days; critical patches within 7–14 days.

### 4. Backup restore success rate
Percentage of scheduled restore tests completed successfully.

**Why useful:** proves whether recovery actually works, not just whether backups exist.  
**Target:** 100% successful monthly restore tests for critical systems.

### 5. Mean time to detect and contain incidents
Time from first alert/report to confirmed containment.

**Why useful:** measures the effectiveness of monitoring and incident response.  
**Target:** detect within 24 hours; contain critical incidents within 8 hours.

## Conclusion

GreenFields currently has **very limited cybersecurity maturity**, and its most serious weaknesses are in governance, identity and access management, network design, backup resilience, detection, and user awareness.

The biggest business risks are ransomware, production disruption, phishing-based account compromise, and failed recovery. A practical 12–18 month improvement plan should focus first on **MFA, removal of shared admin accounts, backup hardening, segmentation, patching, endpoint protection, incident response, and training**.

With disciplined execution, the company can move from an ad hoc security posture to a stable and measurable baseline program within the available **€80,000 annual budget**.
