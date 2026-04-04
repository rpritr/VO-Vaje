# Disaster Recovery Plan (DRP) Template

## 1. Organization Information

- Organization Name: BlueRiver Health Ltd.
- Address:
- IT Department Contact: IT Support – it-support@blueriverhealth.com
- DR Plan Owner: IT Manager
- Date Created: 6st of March 2026
- Last Updated: 6st of March 2026

---

# 2. Purpose

This Disaster Recovery Plan describes the procedures and responsibilities required to recover IT systems and data after a disruption such as cyber attacks, hardware failures, or natural disasters.

The goal is to minimize downtime and data loss while ensuring business continuity.

---

# 3. Scope

This plan applies to the following systems:

| System       | Description            | Criticality |
| ------------ | ---------------------- | ----------- |
| Web server   | Public website         | High        |
| Email system | Internal communication | Medium      |
| File server  | Document storage       | High        |
| ERP system   | Business management    | Critical    |

---

# 4. Disaster Recovery Objectives

| System       | RTO (Recovery Time Objective) | RPO (Recovery Point Objective) |
| ------------ | ----------------------------- | ------------------------------ |
| Web Server   | 2 hours                       | 30 minutes                     |
| Email System | 4 hours                       | 1 hour                         |
| File Server  | 6 hours                       | 2 hours                        |

---

# 5. Disaster Recovery Team

| Role                 | Name | Responsibility          | Contact |
| -------------------- | ---- | ----------------------- | ------- |
| DR Manager           |      | Coordinates recovery    |         |
| System Administrator |      | Restores servers        |         |
| Network Engineer     |      | Restores network        |         |
| Security Officer     |      | Handles cyber incidents |         |

---

# 6. Backup Strategy

| System      | Backup Type | Frequency     | Location        |
| ----------- | ----------- | ------------- | --------------- |
| Database    | Full backup | Daily         | Cloud storage   |
| Web server  | Snapshot    | Every 6 hours | Backup server   |
| File server | Incremental | Daily         | Offsite storage |

Backup locations:

- Cloud backup (AWS / Azure)
- External backup server
- Offline backup (air-gapped storage)

---

# 7. Disaster Scenarios

Possible disasters include:

- Cyber attack (ransomware)
- Hardware failure
- Data corruption
- Network outage
- Power outage
- Natural disaster (fire, flood)

---

# 8. Recovery Procedures

## 8.1 Server Failure

Steps:

1. Identify failed server
2. Activate backup infrastructure
3. Restore latest backup
4. Verify system integrity
5. Reconnect users

---

## 8.2 Ransomware Attack

Steps:

1. Disconnect infected systems
2. Identify affected systems
3. Restore from clean backup
4. Reset passwords
5. Conduct forensic analysis

---

## 8.3 Data Loss

Steps:

1. Identify missing data
2. Retrieve backup
3. Restore database
4. Verify data integrity

---

# 9. Communication Plan

| Situation            | Responsible   | Communication Channel     |
| -------------------- | ------------- | ------------------------- |
| System outage        | IT department | Email / Slack             |
| Major incident       | DR manager    | Phone / Emergency meeting |
| Public communication | Management    | Official statement        |

---

# 10. Testing and Maintenance

The Disaster Recovery Plan must be tested regularly.

| Test Type                    | Frequency |
| ---------------------------- | --------- |
| Backup restore test          | Quarterly |
| Disaster simulation          | Annually  |
| Security incident simulation | Annually  |

---

# 11. Plan Review

This plan should be reviewed:

- After major system changes
- After security incidents
- At least once per year

Responsible person:

---

# 12. Approval

| Name | Role | Signature | Date |
| ---- | ---- | --------- | ---- |
|      |      |           |      |
