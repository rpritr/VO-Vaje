# Disaster Recovery Plan - NetSecure d.o.o.

## 1. Document Control

- Organization Name: NetSecure d.o.o.
- Document Owner: IT Manager
- Approved By: Managing Director
- Version: 1.0
- Review Frequency: Annual or after major incident
- Classification: Internal Confidential

## 2. Purpose

This Disaster Recovery Plan (DRP) defines the procedures, responsibilities and recovery priorities required to restore critical business services after a cyber attack, major system failure, human error, utility outage or loss of office access.

The objective is to restore customer-facing support operations quickly, protect customer and company data, and reduce contractual, financial and reputational impact.

## 3. Scope

This plan applies to the following critical services and supporting systems:

- Microsoft 365 tenant
- PSA / ticketing system
- RMM platform
- Password vault / PAM
- ERP and CRM systems
- Documentation repository
- VPN and remote access services
- Internal file server / NAS and backup repository
- Network, firewall and core identity services
- Admin workstations used for privileged support

## 4. Assumptions

- The company employs 45 staff and supports external business customers under SLA obligations.
- Critical services rely on internet connectivity, cloud platforms and privileged access tools.
- Some systems are SaaS and recovery is limited by the vendor's availability and support model.
- The company must continue at least minimal incident intake and customer communication during an outage.

## 5. Disaster Scenarios

This plan covers:

1. Ransomware affecting internal endpoints or servers
2. Compromise of M365 or privileged identities
3. RMM platform misuse or compromise
4. Failure of internal storage, backup or virtualization hosts
5. Extended outage of ticketing, ERP or CRM platforms
6. Loss of office access, power or connectivity
7. Accidental deletion or corruption of critical documentation

## 6. Roles and Responsibilities

| Role | Primary Responsibility | Backup |
|---|---|---|
| Managing Director | Executive decisions, customer escalation, regulatory decisions | Finance Manager |
| IT Manager (DR Lead) | Coordinates recovery, declares disaster, approves restoration order | Systems Lead |
| Systems Lead | Server, storage, backup and identity restoration | Senior Systems Engineer |
| Network Lead | Firewall, VPN, internet and network restoration | Security Engineer |
| Security Lead | Incident containment, forensics coordination, evidence preservation | IT Manager |
| Service Manager | Customer communication, ticket prioritization, SLA coordination | Service Desk Supervisor |
| Finance Manager | Commercial continuity, insurance, emergency procurement | Managing Director |

## 7. Communication Plan

### Internal Communication
- Primary: mobile phone, Teams (if available), emergency call tree
- Fallback: SMS group and phone conference bridge
- Incident channel owner: Service Manager

### External Communication
- Customers: Service Manager or Account Manager using approved status updates
- Critical customers: direct phone call within 1 hour of confirmed service-impacting disaster
- Vendors: IT Manager or Systems Lead
- Media / regulator / insurer: Managing Director only

## 8. Recovery Priorities

| Priority | Service / System | RTO | RPO | Reason |
|---|---|---:|---:|---|
| 1 | Firewall, VPN and internet connectivity | 4 hours | N/A | Required for all remote support and business operations |
| 2 | Password vault / PAM | 4 hours | 1 hour | Required for secure admin access to internal and customer systems |
| 3 | PSA / Ticketing | 4 hours | 1 hour | Required for incident intake, SLA management and customer coordination |
| 4 | Microsoft 365 | 8 hours | 4 hours | Email, Teams and file collaboration |
| 5 | Documentation repository | 8 hours | 4 hours | Needed for support, projects and accurate restoration |
| 6 | RMM platform | 8 hours | 4 hours | Key tool for customer maintenance and remote response |
| 7 | ERP / CRM | 24 hours | 8 hours | Sales, procurement and finance continuity |
| 8 | Internal file server / NAS | 24 hours | 8 hours | Internal shared data and local exports |
| 9 | Lab / test environment | 72 hours | 24 hours | Important but not essential to immediate continuity |

## 9. Backup Strategy

- Follow the 3-2-1 rule: at least 3 copies, on 2 media types, with 1 offsite/immutable copy.
- Critical backups:
  - M365 exports / SaaS backup where supported
  - Ticketing and documentation exports
  - ERP / CRM database or vendor-supported backups
  - Vault configuration backup
  - NAS and server snapshots
  - Firewall and VPN configuration backup
- Backup credentials must be separate from the primary production identity domain.
- Restore testing:
  - Monthly restore test for one critical system
  - Quarterly restore test for at least one business application
  - Annual full disaster simulation

## 10. Disaster Declaration Criteria

A disaster may be declared by the IT Manager or Managing Director if one or more of the following occur:

- Customer support operations unavailable for more than 2 hours
- Confirmed ransomware, mass encryption or destructive malware
- Confirmed compromise of privileged identity or vault
- Major outage affecting multiple critical systems
- Loss of backup availability or inability to restore critical data
- Legal, contractual or reputational impact requiring formal crisis coordination

## 11. General Response Procedure

### Phase 1 - Detection and Triage
1. Confirm incident scope and severity.
2. Record time of detection and affected assets.
3. Notify DR Lead, Security Lead and Service Manager.
4. Decide whether to activate the DRP.

### Phase 2 - Containment
1. Isolate affected endpoints, accounts or network segments.
2. Suspend risky remote access paths if compromise is suspected.
3. Preserve logs and evidence.
4. Contact key vendors where their platform may be involved.

### Phase 3 - Recovery
1. Restore services in priority order.
2. Validate integrity before reconnecting restored systems.
3. Force credential reset where privileged compromise is possible.
4. Resume customer services in controlled phases.

### Phase 4 - Post-Recovery
1. Verify service stability.
2. Communicate closure status to customers and management.
3. Conduct post-incident review within 5 business days.
4. Update risk register, controls and DR plan based on lessons learned.

## 12. Scenario Playbooks

### 12.1 Ransomware on Internal Systems
1. Disconnect affected devices from network immediately.
2. Disable suspicious user and admin accounts.
3. Block remote access until scope is known.
4. Confirm status of backups before restoration.
5. Rebuild from clean image and restore data from validated backups.
6. Re-enable services gradually with heightened monitoring.

### 12.2 M365 or Identity Compromise
1. Disable compromised accounts and revoke active sessions.
2. Enforce password reset and MFA re-registration.
3. Review inbox rules, OAuth consents and admin changes.
4. Restore deleted mail or files where needed.
5. Notify affected customers if their data or communications were exposed.

### 12.3 RMM Platform Compromise
1. Disable automation, scripts and remote execution.
2. Suspend agent communication if required by vendor guidance.
3. Review command history, packages and target devices.
4. Notify affected customers immediately.
5. Rotate credentials and tokens tied to the platform.
6. Re-enable only after hardening and vendor confirmation.

### 12.4 Loss of Ticketing Platform
1. Switch to emergency intake mailbox and phone hotline.
2. Use emergency spreadsheet log for incident tracking.
3. Prioritize critical customers manually.
4. Restore ticket data from export or vendor recovery.
5. Re-enter emergency records into the platform after recovery.

## 13. Minimum Manual Workarounds

During major outage, the following manual workarounds are permitted:

- Service intake by phone and emergency mailbox
- Temporary incident log in protected spreadsheet
- Phone-based customer status updates
- Critical admin access via break-glass process recorded by DR Lead
- Manual quotation and invoice templates for urgent transactions

## 14. Evidence and Documentation

The following must be documented for every DR activation:

- Start and end time of incident
- Affected systems and business services
- Containment decisions
- Restoration order and validation steps
- Customer notifications
- Root cause and lessons learned

## 15. Testing and Maintenance

| Test Type | Frequency | Owner |
|---|---|---|
| Backup restore test | Monthly | Systems Lead |
| Ransomware tabletop | Semi-annual | Security Lead |
| M365 account compromise exercise | Semi-annual | IT Manager |
| Full DR simulation | Annual | IT Manager |
| Contact list review | Quarterly | Service Manager |

## 16. Approval

- Prepared by: IT Manager
- Reviewed by: Security Lead and Service Manager
- Approved by: Managing Director
- Effective date: 2026-04-05
