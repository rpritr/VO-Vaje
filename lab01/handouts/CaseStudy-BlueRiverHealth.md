# Case Study — BlueRiver Health Ltd.

## 1. Organization Overview

BlueRiver Health Ltd. is a medium-sized private healthcare provider operating in two cities.
It provides:
- outpatient specialist services,
- telemedicine consultations,
- laboratory diagnostics,
- occupational health services for corporate clients.

Employees: 85  
IT staff: 3 (1 IT manager, 2 system administrators)  
Annual revenue: €9M  

## 2. IT Environment

### Infrastructure
- Hybrid environment (on-prem + cloud)
- On-prem:
  - 2 physical servers (VMware)
  - 12 virtual machines
  - Active Directory domain
  - Local NAS backup
- Cloud:
  - Microsoft 365 (email, Teams, SharePoint)
  - SaaS telemedicine platform
  - Cloud-based accounting software

### Endpoints
- 65 Windows laptops
- 20 medical workstations
- 15 mobile tablets
- 8 shared reception PCs

### Network
- Single flat internal network
- Guest WiFi
- VPN access for doctors
- Basic firewall appliance

## 3. Data Types

- Patient medical records (special category data)
- Laboratory results
- Employee HR data
- Financial data
- Corporate client contracts
- Video recordings of telemedicine sessions (stored 30 days)

## 4. Business Processes

1. Patient registration
2. Appointment scheduling
3. Medical examination
4. Laboratory processing
5. Telemedicine consultation
6. Billing & insurance processing

## 5. Known Issues (Past 24 Months)

- 2 phishing incidents (one credential compromise)
- 1 ransomware attempt (blocked)
- Backup restoration never tested
- Doctors share accounts for telemedicine platform
- No formal risk assessment performed
- Security awareness training conducted only once (3 years ago)

## 6. Regulatory Context

- GDPR (special category data)
- National healthcare regulation
- Contractual obligations with insurance companies

## 7. Constraints

- Limited budget
- Resistance from senior doctors to additional controls
- IT team overloaded with daily operations

You are hired as external security consultant to design a lightweight but realistic security governance package.