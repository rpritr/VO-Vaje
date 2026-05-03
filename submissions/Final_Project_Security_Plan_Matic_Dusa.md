# Security Governance Project - Mobik

## 1. Organization Overview
Organization of choice: Mobik d.o.o. 

Mobik is an international telecommunications service provider specializing in revenue assurance, fraud prevention, and advanced network analytics solutions for mobile network operators. 

The company delivers fully managed security and analytics platforms that protect telecom operators from fraud in SMS, voice, OTT, and data traffic. Mobik operates globally and supports hundreds of millions of mobile subscribers through its client base. 

Its core business relies on data processing and real-time network traffic analysis, making information security, data protection, and system availability critical to its operations. 

As a provider of security solutions, Mobik must ensure the confidentiality of sensitive telecom data, integrity of analytical systems, and high availability of its services. 

## 2. Asset Register

| ID | Asset Name | Description | Type | Criticality |
|----|------------|-------------|------|-------------|
| 1 | Telecom Traffic Data | SMS, voice, and data traffic from clients | Data | High |
| 2 | Customer Data | Client information, contracts, and business data | Data | High |
| 3 | Cloud Infrastructure | Hosting environment | Infrastructure | High |
| 4 | Database Servers | Storage for raw and processed telecom data | Infrastructure | High |
| 5 | Internal Network | Company internal communication network | Infrastructure | Medium |
| 6 | Employee Workstations | Laptops and desktops used by employees | Hardware | Medium |
| 7 | Admin Accounts | Privileged system access accounts | Access | High |
| 8 | Monitoring System | Security monitoring and logging system | Software | High |
| 9 | Backup Systems | Data backup and recovery infrastructure | Infrastructure | High |
| 10 | Source Code Repository | Application source code (e.g. Git) | Data | High |
| 11 | CI/CD Pipeline | Automated build and deployment system | Software | High |
| 12 | Email System | Internal and external communication platform | Software | Medium |
| 13 | VPN Access | Secure remote access system | Software | High |
| 14 | Third-party Integrations | External APIs and services | External | Medium |
| 15 | Office Premises | Physical office location | Physical | Low |
| 16 | Security Policies | Internal security documentation and rules | Process | Medium |
| 17 | Incident Response Process | Procedures for handling security incidents | Process | High |
| 18 | Logging Infrastructure | Centralized log systems | Software | High |
| 19 | Encryption Keys | Keys used for securing sensitive data | Data | High |
| 20 | Real-time Processing Engine | System for real-time analysis and processing of telecom traffic data | Software | High |

## 3. Risk Register

| ID | Asset | Risk Description | Impact | Likelihood | Risk Level |
|----|-------|-----------------|--------|------------|------------|
| 1 | Telecom Traffic Data | Unauthorized access which tehn leads to a data breach | High | Medium | High |
| 2 | Customer Data | Exposure of sensitive client information | High | Medium | High |
| 3 | Cloud Infrastructure | Misconfiguration or unauthorized access leading to data exposure | High | Medium | High |
| 4 | Database Servers | Data corruption or loss due to system failure | High | Low | Medium |
| 5 | Internal Network | Unauthorized internal access | Medium | Medium | Medium |
| 6 | Employee Workstations | Malware infection or phishing | Medium | High | High |
| 7 | Admin Accounts | Privilege abuse or account compromise | High | Medium | High |
| 8 | Monitoring System | Failure to detect security incidents | High | Medium | High |
| 9 | Backup Systems | Backup failure or data not being recoverable | High | Low | Medium |
| 10 | Source Code Repository | Unauthorized code access or data leakage | High | Medium | High |
| 11 | CI/CD Pipeline | Compromised pipeline leading to malicious code deployment | High | Low | Medium |
| 12 | Email System | Phishing attacks targeting employees | Medium | High | High |
| 13 | VPN Access | Unauthorized remote access to internal systems | High | Medium | High |
| 14 | Logging Infrastructure | Logs tampered or deleted to hide attacks | High | Medium | High |
| 15 | Encryption Keys | Compromise of keys leading to data exposure | High | Low | Medium |
| 16 | Real-time Processing Engine | System overload or failure causing missed fraud detection | High | Medium | High |

## 4. Control Mapping

| ID | Risk ID | Control Name | Description |
|----|---------|--------------|-------------|
| 1 | 1 | Data Encryption | Encrypt telecom traffic data at rest and in transit |
| 2 | 2 | Access Control Policy | Restrict access to customer data using role-based access control (RBAC) |
| 3 | 3 | Cloud Security Configuration | Enforce secure cloud configurations and perform regular audits |
| 4 | 4 | Database Backup & Recovery | Implement regular backups and data integrity checks |
| 5 | 5 | Network Access Control | Restrict and monitor internal network access |
| 6 | 6 | Endpoint Protection | Deploy antivirus and EDR solutions on employee devices |
| 7 | 7 | Privileged Access Management | Monitor and control usage of admin accounts |
| 8 | 8 | Monitoring | Implement centralized logging and real-time monitoring |
| 9 | 9 | Backup Testing | Regularly test backup restoration procedures |
| 10 | 10 | Repository Access Control | Limit access to source code and enforce authentication |
| 11 | 11 | Secure CI/CD Pipeline | Implement code scanning and integrity validation in pipeline |
| 12 | 12 | Security Awareness Training | Train employees to recognize phishing attacks |
| 13 | 13 | Multi-Factor Authentication (MFA) | Enforce MFA for remote and VPN access |
| 14 | 14 | Log Integrity Controls | Protect logs from unauthorized modification or deletion |
| 15 | 15 | Key Management System (KMS) | Secure storage, rotation, and management of encryption keys |
| 16 | 16 | Load Balancing & System Scaling | Ensure system availability under high load conditions |

## 5. Policies

### 5.1 Access Control Policy

**Purpose:**  
To ensure that access to systems and data is restricted to authorized users only.

**Scope:**  
Applies to all employees and systems within Mobik and their clients.

**Policy:**
- Access must be granted based on the principle of least privilege
- Role-Based Access Control (RBAC) must be enforced
- Administrative access must be limited and monitored
- Multi-Factor Authentication (MFA) is required for critical systems

**Responsibilities:**
- IT team manages access rights
- Employees must not share credentials adn must be careful with their information


### 5.2 Incident Response Policy

**Purpose:**
To ensure timely detection and response to security incidents.

**Scope:**
Applies to all systems and employees.

**Policy:**
- All incidents must be reported immediately
- Security team must investigate and respond
- Logs must be preserved for analysis
- Incidents must be documented and reviewed

**Responsibilities:**
- Security team handles incidents
- Employees report any suspicious activity


### 5.3 Acceptable Use Policy

**Purpose:**
To define acceptable use of company systems.

**Scope:**
Applies to all employees and devices.

**Policy:**
- Systems/Devices must be used for business purposes only
- Unauthorized software installation is prohibited
- Users must not access malicious or illegal content
- Devices must be secured at all times

**Responsibilities:**
- Employees must follow usage rules
- IT monitors compliance of rules


### 5.4 Backup Policy

**Purpose:**
To ensure availability and recovery of data.

**Scope:**
Applies to all critical systems and data.

**Policy:**
- Regular backups must be performed
- Backups must be securely stored
- Backup integrity must be tested regularly
- Recovery procedures must be documented

**Responsibilities:**
- IT team manages backups
- Management ensures compliance


### 5.5 Password Policy

**Purpose:**
To enforce strong authentication practices.

**Scope:**
Applies to all users and systems.

**Policy:**
- Passwords must meet complexity requirements
- Password reuse is not allowed
- Passwords must be changed periodically
- MFA must be used where possible

**Responsibilities:**
- Users must protect their credentials nad be responsible with their information
- IT enforces password policies

## 6. Business Impact Analysis (BIA)

| ID | Asset | Business Impact | Max Downtime (RTO) | Data Loss Tolerance (RPO) | Priority |
|----|-------|----------------|--------------------|---------------------------|----------|
| 1 | Telecom Traffic Data | Loss impacts fraud detection accuracy and service quality | 1 hour | Near zero | High |
| 2 | Customer Data | Legal, financial, and reputational damage | 4 hours | Low | High |
| 3 | Cloud Infrastructure | Full/Partial service outage across all systems | 1 hour | Low | High |
| 4 | Database Servers | Data unavailable for analytics and operations | 2 hours | Low | High |
| 5 | Internal Network | Disruption of internal communication and operations | 8 hours | Medium | Medium |
| 6 | Employee Workstations | Reduced productivity of employees | 24 hours | Medium | Low |
| 7 | Admin Accounts | Loss of control over systems and infrastructure | 1 hour | Near zero | High |
| 8 | Monitoring System | Inability to detect and respond to threats | 2 hours | Low | High |
| 9 | Backup Systems | Inability to restore lost or corrupted data | 4 hours | Low | High |
| 10 | Source Code Repository | Loss of development data and delays in releases | 8 hours | Low | Medium |
| 11 | CI/CD Pipeline | Inability to deploy updates and fixes | 8 hours | Medium | Medium |
| 12 | Email System | Disruption of comunication | 24 hours | Medium | Low |
| 13 | VPN Access | Remote work disruption and access problems | 4 hours | Medium | Medium |
| 14 | Third-party Integrations | Service disruption | 8 hours | Medium | Medium |
| 15 | Office Premises | Physical access not available to the workplace | 48 hours | N/A | Low |
| 16 | Security Policies | Lack of guidance leading to inconsistent security practices | 72 hours | N/A | Low |
| 17 | Incident Response Process | Delayed response to incidents and increased loss | 1 hour | N/A | High |
| 18 | Logging Infrastructure | Loss of visibility and audit trail | 2 hours | Low | High |
| 19 | Encryption Keys | Data exposure and loss of confidentiality | Immediate | Near zero | High |
| 20 | Real-time Processing Engine | Failure to detect fraud in real time | 1 hour | Near zero | High |

## 7. Disaster Recovery Plan

### 7.1 Purpose

The purpose of this disaster recovery plan is to ensure that Mobik can quickly recover critical systems and resume operations in the event of a major disruption.

---

### 7.2 Scope

This plan applies to all critical systems, including:
- Cloud Infrastructure
- Database Servers
- Telecom Traffic Data
- Monitoring System

---

### 7.3 Incident Types

This plan covers:
- Cyberattacks
- System failures
- Cloud service outages
- Network disruptions

---

### 7.4 Roles and Responsibilities

- **IT Team** - system and infrastructure recovery
- **Security Team** - incident investigation and containment
- **Management** - decision making and communication

---

### 7.5 Recovery Strategy

#### Step 1 - Detection
- Identify the incident
- Analyze logs and alerts

#### Step 2 - Containment
- Isolate affected systems

#### Step 3 - Recovery
- Restore systems from backups
- Rebuild infrastructure if necessary
- Validate system integrity

#### Step 4 - Communication
- Inform managemen
- Notify affected clients if required

#### Step 5 - Post-Incident Review
- Analyze root cause
- Improve controls, processes and policies

---

### 7.6 Recovery Priorities

| Priority | System |
|----------|--------|
| 1 | Database Servers |
| 2 | Real-time Processing Engine |
| 3 | Telecom Traffic Data |
| 4 | Monitoring System |

---

### 7.7 Backup Strategy

- Daily backups of critical data
- Secure off-site storage
- Regular backup testing

---

### 7.8 Testing and Maintenance

- DR plan must be tested annually
- Updates must be made after major system changes or incidents

## 8. Loom Video

https://www.loom.com/share/f0b7246c45bc4b4497f0ed66950c1d0a