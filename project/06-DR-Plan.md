# GreenFields Food Processing Ltd. - Disaster Recovery Plan

**Document ID:** GF-DR-001  
**Owner:** IT Manager  
**Approved By:** Managing Director  
**Version:** 1.0  
**Review Date:** Annual or after any major incident or significant system change

---

## 1. Purpose

This Disaster Recovery Plan defines how GreenFields Food Processing Ltd. restores critical IT services after cyberattack, system failure, environmental disruption, or other major outage.

The objectives are to:
- protect life and food safety first
- minimize production downtime
- restore critical business services in priority order
- preserve evidence during cyber incidents
- meet contractual and regulatory obligations

---

## 2. Scope

This plan applies to:
- headquarters and both production plants
- on-premise infrastructure including virtualization hosts, servers, network equipment, and backups
- critical business systems including ERP, WMS, Microsoft 365, file services, payroll, recipe/specification data, and quality records
- supporting connectivity including VPN and internet access

This plan complements but does not replace the Incident Response Policy.

---

## 3. Planning Assumptions

- GreenFields has limited IT staffing and must use clear escalation paths.
- Production downtime should be minimized, but unsafe recovery shortcuts are not permitted.
- Critical backups must exist in both local and isolated offsite form.
- Recovery priorities are based on business impact, traceability obligations, and customer delivery commitments.
- In a suspected cyber event, recovery must not begin until containment and scope assessment are sufficient to avoid reinfection.

---

## 4. Disaster Recovery Team

| Role | Primary Responsibility |
|---|---|
| Managing Director | Executive decision making, crisis approval, external escalation |
| IT Manager | DR lead, activation decision support, technical coordination |
| System Administrator | Server, backup, identity, and restore execution |
| Network Administrator or Service Provider | Firewall, switching, segmentation, internet recovery |
| Production Manager | Production impact assessment and plant coordination |
| Quality Manager | Food safety, batch release, traceability controls |
| Warehouse Manager | Receiving, dispatch, and manual fallback coordination |
| HR Manager | Employee communication support and staffing coordination |
| External Vendors | Specialist support for backup platform, firewall, ERP, or forensics |

> Maintain an offline contact list with names, mobile numbers, vendors, and escalation paths.

---

## 5. Activation Criteria

This plan may be activated when one or more of the following occur:
- production or dispatch cannot operate for more than 30 minutes due to IT outage
- ransomware or widespread malware is suspected
- a critical server, network core, or identity service fails
- backup integrity is in doubt after a major incident
- building, power, or environmental failure affects the server room
- management declares a major operational disruption

**Activation Authority:** Managing Director or IT Manager  
**Severity Levels:** Medium, High, Critical

---

## 6. Recovery Objectives

| Service or System | Business Purpose | RTO Hours | RPO Hours | Recovery Priority |
|---|---|---:|---:|---:|
| Firewall and core network | Foundation for all other services | 2 | N/A | 1 |
| Active Directory and identity services | User and system authentication | 2 | 1 | 1 |
| ERP system | Production planning, inventory, finance | 4 | 1 | 1 |
| Production line control connectivity | Plant operations and supervision | 4 | 1 | 1 |
| Recipe and specification database | Product integrity and labeling control | 4 | 1 | 1 |
| WMS and handheld scanning | Receiving, stock control, dispatch | 6 | 2 | 2 |
| File server and quality records | Procedures, QA evidence, shared documents | 8 | 4 | 2 |
| Microsoft 365 | Email, Teams, document collaboration | 12 | 4 | 3 |
| Payroll system | Employee payment processing | 48 | 24 | 4 |
| CCTV and access control | Physical security support | 24 | 8 | 4 |

---

## 7. Backup Strategy

### 7.1 Minimum Requirements
- Apply the **3-2-1** principle.
- Keep one immutable or offline backup copy.
- Use separate credentials for backup administration.
- Encrypt backups in transit and at rest.
- Back up critical configurations including firewall rules, switch configs, VPN settings, and virtualization settings.

### 7.2 Backup Frequency
- **ERP, Active Directory, recipe database, file server, WMS, QA records:** daily backup
- **Critical virtual machine snapshots or image-based backups:** daily
- **Configuration backups:** after every significant change and at least weekly
- **Microsoft 365 key data:** according to approved backup or export capability

### 7.3 Restore Testing
- Critical restore test: monthly
- Non-critical restore test: quarterly
- Full DR exercise: annually

---

## 8. Recovery Priorities by Business Process

1. Production and packing operations  
2. Quality control and batch release  
3. Raw material receiving and traceability  
4. Warehouse dispatch and shipping  
5. Production planning and scheduling  
6. Order intake and customer service  
7. Procurement and supplier coordination  
8. Finance and payroll  

---

## 9. Initial Response Checklist

### First 15 Minutes
- Confirm incident and classify severity.
- Ensure safety of people and any plant process implications.
- Notify DR lead and Managing Director.
- If cyber-related, isolate affected systems or network segments immediately.
- Preserve evidence where possible.
- Start incident log with time, reporter, systems affected, and actions taken.

### First 30 Minutes
- Determine whether the outage is cyber, infrastructure, application, or environmental.
- Identify affected business processes and sites.
- Check status of backups and last known good restore points.
- Decide whether to activate manual workarounds for production, warehouse, or quality teams.
- Notify key business owners.

### First 60 Minutes
- Establish recovery bridge or conference call.
- Assign technical recovery workstreams.
- Assign internal communication owner.
- Escalate to vendors if needed.
- Prepare management update with current impact, expected recovery path, and major risks.

---

## 10. Scenario-Based Recovery Procedures

### 10.1 Ransomware or Widespread Malware

1. Isolate infected endpoints, servers, or VLANs.
2. Disable compromised accounts and block remote access if required.
3. Confirm whether backups are safe and not encrypted.
4. Preserve logs, ransom notes, suspicious emails, and timeline evidence.
5. Rebuild or restore only from known-clean images and backups.
6. Prioritize recovery of network, identity, ERP, recipe database, WMS, and quality records.
7. Force password resets for privileged and potentially affected users.
8. Validate restored systems before reconnecting them to production.
9. Conduct lessons learned and close the attack vector before full return to normal.

**Do not pay ransom without executive and legal review.**

---

### 10.2 Virtual Host or Server Failure

1. Identify failed host or virtual machine.
2. Move critical workloads to surviving infrastructure where feasible.
3. Restore from backup if failover is not possible.
4. Verify application integrity and business function.
5. Document root cause and repair or replace hardware.

---

### 10.3 Network Core or Firewall Failure

1. Confirm whether the issue is ISP, firewall, switch, or internal routing.
2. Restore last known good firewall or switch configuration if needed.
3. Recover internet edge and site routing first.
4. Verify segregation between corporate, production, and guest networks.
5. Reconnect critical systems in priority order.

---

### 10.4 Lost or Stolen Laptop

1. Report immediately to IT Manager.
2. Disable user session tokens and high-risk access if applicable.
3. Attempt remote lock or remote wipe.
4. Assess whether regulated or sensitive information was exposed.
5. Reissue device only after user account review and password reset.

---

### 10.5 Backup Failure or Suspected Corruption

1. Stop any backup jobs that may propagate corruption.
2. Verify last successful clean backup and offsite copy.
3. Conduct an isolated restore test.
4. Escalate if RPO cannot be met.
5. Record corrective action for backup process improvement.

---

## 11. Manual Workarounds

| Process | Manual Fallback |
|---|---|
| Order intake | Phone and paper order logs |
| Receiving | Paper goods-in register and lot capture |
| Production scheduling | Printed production board and supervisor coordination |
| Quality checks | Controlled paper forms and later reconciliation |
| Dispatch | Manual pick lists and shipment logs |
| Internal communication | Phone tree and SMS list |

Manual workarounds must be reconciled back into core systems once systems are restored.

---

## 12. Communication Plan

### Internal
- Managing Director receives executive updates at agreed intervals.
- Department heads receive impact and workaround updates.
- Staff receive clear instructions on what systems they may or may not use.

### External
- Customers: only for material service impact or delivery delays
- Critical suppliers and logistics partners: if schedules or interfaces are affected
- Insurers: according to policy conditions
- Regulators or authorities: as required by applicable law or incident type
- Media: only through authorized management spokesperson

---

## 13. Recovery Validation

Before declaring recovery complete:
- confirm restored systems are functioning as intended
- confirm data integrity checks are completed
- verify access controls and MFA are enforced
- verify monitoring and logging are re-enabled
- validate production, QA, warehousing, and dispatch workflows
- obtain business owner sign-off for critical services

---

## 14. Post-Incident Review

Within 5 business days of closure:
- document timeline, root cause, impact, and decisions
- identify control failures and improvement actions
- update risk register, DR plan, and playbooks as needed
- report lessons learned to management

---

## 15. Testing and Maintenance

| Activity | Frequency | Owner |
|---|---|---|
| Backup restore test for critical systems | Monthly | IT Manager |
| Backup restore test for non-critical systems | Quarterly | System Administrator |
| DR tabletop exercise | Semi-annual | IT Manager |
| Full DR exercise | Annual | Managing Director and IT Manager |
| Contact list review | Quarterly | HR Manager |
| Plan review | Annual or after major change | IT Manager |

---

## 16. Approval

| Name | Role | Signature | Date |
|---|---|---|---|
|  | Managing Director |  |  |
|  | IT Manager |  |  |
|  | Production Manager |  |  |
|  | Quality Manager |  |  |