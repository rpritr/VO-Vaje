# GreenFields Food Processing Ltd. - Security Policy Pack

**Document Owner:** IT Manager  
**Approved By:** Managing Director  
**Review Cycle:** Annual or after a major incident  
**Applies To:** All employees, contractors, temporary staff, and third parties with access to GreenFields systems or data

---

## 1. Information Security Governance Policy (GF-POL-001)

### Purpose
To establish the minimum governance structure required to manage information security risk in a consistent and defensible manner.

### Policy Statements
- GreenFields shall maintain a documented asset register, risk register, control mapping, and incident log.
- Management shall review security risks, incidents, and key metrics at least quarterly.
- Each critical asset shall have a named business owner and a named technical owner where applicable.
- Security decisions shall be risk-based and aligned to business continuity needs for production, quality, warehousing, and distribution.
- Exceptions to policy must be documented, approved by management, and reviewed every 90 days.

### Roles and Responsibilities
- **Managing Director:** approves risk tolerance and major remediation funding.
- **IT Manager:** maintains governance records and coordinates implementation.
- **Business Owners:** accept or escalate residual risk for their processes.
- **All Staff:** comply with policies and report security concerns.

### Compliance
Non-compliance may lead to disciplinary action, supplier escalation, or removal of system access.

---

## 2. Access Control and Identity Policy (GF-POL-002)

### Purpose
To ensure only authorized users have access to company systems and data, and only to the extent needed for their role.

### Policy Statements
- Every user must have a unique named account. Shared user or administrator accounts are prohibited except for tightly controlled emergency break-glass access.
- Multi-factor authentication is mandatory for Microsoft 365, VPN, ERP, privileged accounts, and any externally accessible system.
- Access rights shall follow least privilege and role-based access control.
- Privileged access shall be restricted to authorized IT personnel and reviewed quarterly.
- New joiners must receive only approved access based on role. Leavers must have all access removed within 24 hours.
- Passwords must be at least 12 characters or use approved passphrases. Reuse of shared or generic credentials is prohibited.
- Service accounts must be documented, owner-assigned, and reviewed at least every six months.

### User Responsibilities
- Users must not share credentials or approve MFA prompts they did not initiate.
- Users must lock workstations when unattended.
- Users must immediately report suspected credential theft.

### Verification
Quarterly access review, monthly MFA coverage review, and audit of privileged accounts.

---

## 3. Acceptable Use and Endpoint Security Policy (GF-POL-003)

### Purpose
To define acceptable use of company technology and minimum protection requirements for user devices.

### Policy Statements
- Company IT systems are for authorized business use only.
- Users must not install unauthorized software, disable security tools, or bypass company controls.
- Laptops and smartphones used for company work must be enrolled in approved management controls where supported.
- Full-disk encryption shall be enabled on all company laptops and mobile devices that store or access business data.
- Devices shall auto-lock after a maximum of 10 minutes of inactivity.
- USB media use shall be restricted to approved business need and scanned before use.
- Production line PCs may only run approved software and may not be used for web browsing or personal email unless explicitly authorized.
- Lost or stolen devices must be reported immediately.

### Prohibited Activities
- Sharing accounts or passwords
- Using personal cloud storage for company data
- Connecting unauthorized devices to internal or production networks
- Opening suspicious email attachments or links without validation

### Verification
Device compliance reporting, spot checks, and incident review.

---

## 4. Backup, Recovery, and Retention Policy (GF-POL-004)

### Purpose
To ensure critical systems and data can be restored in a timely and reliable manner after cyber incidents, system failure, or human error.

### Policy Statements
- GreenFields shall follow the **3-2-1** backup principle: three copies of data, on two media types, with one copy offsite or otherwise isolated.
- Critical systems including ERP, WMS, Active Directory, file server, recipe database, and quality records must be backed up daily.
- At least one backup copy must be immutable or offline and protected by separate credentials.
- Backup data must be encrypted at rest and in transit.
- Restore tests for critical systems shall be performed monthly; non-critical restore tests shall be performed quarterly.
- Backup retention periods must support operational, contractual, and regulatory needs.
- Failed backups or failed restore tests must be escalated within one business day.

### Minimum Backup Scope
- System configuration backups
- Virtual machine backups
- Application data backups
- Key exportable cloud data where technically feasible
- Network and firewall configuration backups

### Verification
Backup success reports, restore test evidence, and annual DR exercise results.

---

## 5. Incident Response and Reporting Policy (GF-POL-005)

### Purpose
To ensure security incidents are reported, contained, investigated, and recovered from in a coordinated and timely manner.

### Policy Statements
- All employees must immediately report suspected incidents to IT.
- Incidents include phishing, malware, lost devices, unauthorized access, unusual system behavior, data leakage, and operational disruption linked to IT.
- The IT Manager shall maintain an incident register and severity classification process.
- High and critical incidents shall have assigned incident leads, containment actions, communication owners, and post-incident reviews.
- Evidence must be preserved where feasible. Infected systems should be isolated, not wiped, until triage is complete unless safety or operations demand faster action.
- Management must be informed promptly of incidents affecting production, customer commitments, regulated data, or significant financial impact.
- External notifications to customers, insurers, regulators, or suppliers shall be coordinated by management and legal or privacy representatives as needed.

### Response Targets
- Triage of reported incident: within 30 minutes during business hours
- Initial containment for high or critical incidents: within 4 hours where feasible
- Post-incident review: within 5 business days of closure

### Verification
Incident log quality, tabletop exercises, corrective action tracking.

---

## 6. Vendor and Third-Party Security Policy (GF-POL-006)

### Purpose
To reduce the risk introduced by suppliers, service providers, logistics partners, and outsourced support.

### Policy Statements
- Critical suppliers with network connectivity, data access, or operational dependency must undergo security review before onboarding and at least annually thereafter.
- Contracts with critical vendors should include confidentiality terms, incident notification requirements, minimum security expectations, and termination or access revocation provisions.
- Third-party remote access must be approved, time-bound where possible, and protected by MFA.
- Vendors shall receive only the minimum access needed to deliver their service.
- High-risk vendors should be prioritized based on business impact to production, warehousing, quality, finance, or customer data.
- Security findings from suppliers must be tracked to closure or risk acceptance.

### Verification
Vendor register, review checklist, contract evidence, and access audit.

---

## 7. Patch and Vulnerability Management Policy (GF-POL-007)

### Purpose
To reduce exposure to known vulnerabilities while minimizing disruption to food production operations.

### Policy Statements
- GreenFields shall maintain an inventory of systems in scope for patching and vulnerability review.
- Critical security patches should be applied within 7 days where compatible and operationally feasible.
- Standard monthly patch cycles shall apply to endpoints, servers, and supported infrastructure.
- Production systems requiring maintenance windows must follow a documented testing and scheduling process.
- Exceptions must be approved by the asset owner and IT Manager, with compensating controls where needed.
- Unsupported software or operating systems must be identified, risk-assessed, and replaced or isolated.

### Verification
Monthly patch compliance dashboard, exception register, vulnerability review notes.

---

## Policy Acknowledgement
All personnel must read and acknowledge policies relevant to their role. Managers are responsible for reinforcing compliance within their teams.