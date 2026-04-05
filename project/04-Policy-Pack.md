# Policy Pack - NetSecure d.o.o.

This minimum viable policy pack establishes a practical governance baseline for a 45-person IT company providing equipment sales, system integration, security integration, support and maintenance services.

## 1. Access Control Policy

### Purpose
To ensure that access to company and customer systems is granted on a need-to-know and least-privilege basis.

### Core Rules
- Every user must have an individual named account.
- Shared administrative accounts are prohibited unless a documented break-glass exception is approved.
- MFA is mandatory for Microsoft 365, VPN, ticketing, ERP, vault and all privileged accounts.
- Privileged access must be performed from managed admin workstations where feasible.
- Access rights must be reviewed at least quarterly.
- Accounts must be disabled within 24 hours of employee departure and immediately for high-risk terminations.

## 2. Acceptable Use Policy

### Purpose
To define the permitted use of company devices, accounts and information assets.

### Core Rules
- Company IT resources are for authorized business use only.
- Users must not install unauthorized software or browser extensions.
- Users must not store customer documentation or credentials in personal cloud services or local unmanaged files.
- Devices must be locked when unattended.
- Suspicious emails, MFA prompts, remote access requests and unusual customer incidents must be reported immediately.
- Users must not bypass security controls or share passwords.

## 3. Backup and Recovery Policy

### Purpose
To ensure recoverability of critical data and services after accidental deletion, cyber incidents or system failure.

### Core Rules
- Critical systems and data must be backed up according to the 3-2-1 principle.
- Backup copies must include at least one offsite or immutable copy.
- Backup credentials must be separate from the main production domain.
- Restore tests must be performed monthly for critical systems and documented.
- Failed backup or restore tests must be escalated to the IT Manager within one business day.
- Recovery priorities must align with the approved BIA and DR Plan.

## 4. Incident Response Policy

### Purpose
To provide a consistent process for detecting, reporting, triaging, containing and recovering from security incidents.

### Core Rules
- All employees must report suspected incidents immediately.
- Security incidents include phishing, malware, account compromise, data leakage, lost devices, unauthorized access and customer-impacting outages with a security dimension.
- The IT Manager is the incident owner unless delegated.
- Incidents must be classified by severity and recorded in the incident register.
- Evidence must be preserved before destructive actions when feasible.
- Customer communication must be coordinated through the Service Manager or Account Manager.
- Regulatory or contractual notification obligations must be evaluated for every data-related incident.

## 5. Data Classification and Handling Policy

### Purpose
To protect internal and customer information according to business sensitivity.

### Classification Levels
- Public
- Internal
- Confidential
- Restricted

### Core Rules
- Customer network diagrams, security configurations, credentials, contracts, HR data and finance records must be classified at least Confidential, with the most sensitive items marked Restricted.
- Restricted data must only be stored in approved repositories with controlled sharing.
- Sensitive exports must have an owner and retention period.
- Access to documentation repositories and tickets containing sensitive customer data must be role-based.
- Information must be deleted or archived according to business, legal and contractual requirements.

## 6. Vendor Security Policy

### Purpose
To reduce third-party risk from vendors, distributors, SaaS providers and subcontractors.

### Core Rules
- Critical vendors must undergo a documented security review before onboarding.
- Contracts with relevant vendors must include confidentiality, breach notification and data protection clauses.
- Integrations with third-party tools must use scoped permissions where possible.
- Vendor access must be reviewed regularly and removed when no longer required.
- Critical suppliers supporting customer-facing services must be recorded in the vendor register with owner and review date.

## 7. Patch and Vulnerability Management Policy

### Purpose
To reduce the risk of exploitation from known weaknesses.

### Core Rules
- Critical security patches must be applied within 7 days unless an approved exception exists.
- Standard patches must be applied within 30 days.
- Internet-facing systems, admin workstations and security tooling receive priority.
- Vulnerability scans must be reviewed regularly and tracked to closure.
- Exceptions must be documented with risk owner approval and compensating controls.

## 8. Joiner-Mover-Leaver Policy

### Purpose
To ensure timely provisioning, change and removal of access throughout the employment lifecycle.

### Core Rules
- HR and IT must use a formal checklist for onboarding and offboarding.
- New access must be role-based and approved by a manager.
- Role changes must trigger access review.
- Departed staff must return devices and lose all logical access promptly.
- Shared secrets known to departed staff must be rotated where relevant.
