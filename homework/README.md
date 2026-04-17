# Homework — Security Improvement Plan

## Objective

You are hired as an external cybersecurity consultant.  
Your task is to evaluate the current security posture of the organization and propose a **practical security improvement plan**.

The plan should focus on **realistic improvements that could be implemented within 12–18 months**.

---

## Organization Case Study — GreenFields Food Processing Ltd.

### Company Overview

GreenFields Food Processing Ltd. is a medium-sized food production company that produces packaged organic food products for European supermarkets.

- Employees: 120  
- Locations: 2 production plants + 1 headquarters  
- Annual revenue: €25M  

The company recently started expanding internationally and relies increasingly on digital systems.

---

### IT Environment

#### Infrastructure

- 1 small on-prem server room
- 4 virtualization hosts
- 20 virtual machines

Main systems:

- ERP system (production and logistics)
- Warehouse management system
- Microsoft 365 (email, SharePoint, Teams)
- File server for internal documents
- Payroll system

---

#### Endpoints

- 90 Windows laptops
- 30 industrial production PCs
- 20 warehouse handheld scanners
- 15 smartphones for managers

---

#### Network

- One main corporate network
- Production network connected to the same LAN
- Guest WiFi for visitors
- Remote VPN access for managers

No network segmentation currently implemented.

---

### Security Situation

The organization currently has **very limited cybersecurity maturity**.

Observations:

- No formal risk assessment has ever been performed
- No security policies exist
- Shared administrator passwords are used
- Backup exists but is stored on the same network
- No security monitoring
- No incident response plan
- Employees receive no security training
- Patch management is inconsistent
- Production network connected directly to corporate network

---

### Recent Incidents

In the past 12 months:

- One ransomware incident at a supplier
- One phishing email caused an employee to enter credentials on a fake website
- One laptop containing internal documents was lost during travel

---

### Constraints

The company has the following constraints:

- IT team consists of only **3 people**
- Security budget estimated at **€80,000 per year**
- Production downtime must be minimized
- Management wants improvements but fears operational disruption

---

## Your Task

Prepare a **Security Improvement Plan** for the organization.

Your plan should include:

### 1. Security Maturity Assessment

GreenFields is currently operating with significant security gaps across all areas, which makes it highly vulnerable to modern cyber threats. The company does not have a clear security strategy or defined responsibilities for cybersecurity. 
There is a high risk of unauthorized access because of shared administrator passwords and weak access control. The network is not segmented, meaning everything is connected in one network. This allows attackers to move easily between systems, which is especially dangerous in case of a ransomware attack.
Many systems are also vulnerable to known exploits due to inconsistent patching. Although backups exist, they are stored on the same network, which makes them unreliable in case of a cyberattack.
The company does not have any monitoring in place, so it may not even notice when an attack is happening. In addition, there is no incident response plan, which means that any response to an attack would likely be slow and unorganized, increasing the overall damage.
Employees also represent a weak point, since they are not trained in cybersecurity and have already been targeted by phishing attacks.
Overall, the organization is especially exposed to ransomware, phishing and credential theft, insider misuse, and potential disruptions to production systems.

---

### 2. Top 10 Security Risks

The most important cybersecurity risks, described in general terms and supported with examples from the GreenFields case study.
1.	Weak Security Governance and Lack of Policies
Organizations without clear security policies and defined responsibilities often have inconsistent and ineffective security practices.
Example: GreenFields has no formal security policies or risk assessments.
2.	Weak Identity and Access Management
Poor access control increases the risk of unauthorized access and privilege misuse.
Example: Shared administrator passwords are used, and no MFA is implemented.
3.	Lack of Network Segmentation
Flat networks allow attackers to move laterally between systems after initial access.
Example: Production systems, corporate network, and guest WiFi are all connected to the same LAN.
4.	Phishing and Social Engineering Attacks
Employees are often the weakest link if they are not properly trained to recognize attacks.
Example: An employee entered credentials on a phishing website.
5.	Absence of Multi-Factor Authentication (MFA)
Without MFA, compromised passwords can easily lead to full account takeover.
Example: Systems like Microsoft 365 and VPN likely rely only on passwords.
6.	Poor Patch and Vulnerability Management
Unpatched systems are vulnerable to known exploits and malware.
Example: Patch management at GreenFields is inconsistent.
7.	Inadequate Backup and Recovery Strategy
Backups must be protected and separated to ensure recovery after incidents.
Example: Backups are stored on the same network, making them vulnerable to ransomware.
8.	Lack of Security Monitoring and Detection
Without monitoring, attacks may go unnoticed for long periods.
Example: GreenFields has no security monitoring or logging in place.
9.	Missing Incident Response Plan
Organizations without a response plan react slowly and inefficiently to incidents.
Example: No incident response procedures are defined.
10.	Unsecured Endpoints and Data Loss Risks
Devices without proper security controls can lead to data breaches if lost or stolen.
Example: A company laptop containing internal data was lost during travel.

---

### 3. Priority Security Improvements

Below are 10 concrete security improvements that GreenFields should implement. Each measure addresses key risks identified earlier.
1.	Develop Basic Security Policies
GreenFields should create essential security policies (e.g. password policy, access control, backup policy).
Policies provide clear rules and responsibilities, ensuring consistent and secure behavior across the organization.
2.	Eliminate Shared Accounts and Improve Access Control
Each user should have individual accounts, and admin privileges should be limited.
This improves accountability and reduces the risk of misuse or unauthorized access.
3.	Introduce Network Segmentation
Separate corporate, production, and guest networks.
Limits the spread of attacks (e.g. ransomware) and protects critical production systems.
4.	Conduct Employee Security Awareness Training
Train employees on phishing, password security, and safe behavior.
Reduces human error, which is one of the most common causes of security incidents.
5.	Implement Multi-Factor Authentication (MFA)
Enable MFA for Microsoft 365, VPN access, and administrative accounts.
MFA significantly reduces the risk of account compromise, especially from phishing attacks.
6.	Establish Patch Management Process
Implement regular and centralized patching for all systems.
Reduces exposure to known vulnerabilities and common attack methods.
7.	Improve Backup Strategy (3-2-1 Rule)
Store backups offline or in a separate environment (e.g. cloud).
Ensures data can be recovered even in case of ransomware.
8.	Implement Basic Security Monitoring
Enable logging and use a simple monitoring solution (e.g. Microsoft Defender tools).
Provides visibility into attacks and enables faster detection and response.
9.	Implement an Incident Response Plan
The company should develop and document procedures for detecting, responding to, and recovering from security incidents.
This ensures faster and more organized response, reducing damage and downtime.
10.	Deploy Endpoint Protection (EDR/Antivirus)
Install modern endpoint protection on laptops and production PCs.
Detects and blocks malware, ransomware, and suspicious activity.

---

### 4. Implementation Roadmap

Create a **12–18 month implementation plan**.
The implementation is divided into three phases to ensure gradual improvement without disrupting business operations.
Phase 1 — Immediate Improvements (0–3 months)
It focuses on quick wins + biggest risk reduction. 
Key actions:
•	Develop basic security policies (passwords, access, backups) 
•	Enable Multi-Factor Authentication (MFA) for Microsoft 365 and VPN 
•	Remove shared administrator accounts 
•	Start regular patching of critical systems 
•	Provide basic security awareness training (phishing) 
•	Secure endpoints (enable disk encryption, screen lock policies)
These measures are low-cost, quick to implement, and significantly reduce the risk of phishing attacks, unauthorized access and basic malware infections.
Phase 2 — Medium-Term Improvements (3–9 months)
It focuses on building core security capabilities.
Key actions:
•	Perform a formal risk assessment 
•	Implement network segmentation (separate production, corporate, guest) 
•	Improve backup strategy (offline / cloud backups, test recovery) 
•	Deploy endpoint protection (EDR/antivirus) 
•	Introduce basic logging and monitoring (e.g. Microsoft tools)
This phase strengthens the organization’s ability to prevent lateral movement (ransomware spread), detect suspicious activity and recover from incidents.
Phase 3 — Strategic Improvements (9–18 months)
It focuses on maturity and long-term resilience.
Key actions:
•	Develop and test an Incident Response Plan 
•	Conduct advanced employee training (simulated phishing) 
•	Define access control model (least privilege) 
•	Regular security audits and reviews 
•	Improve documentation and security processes
These measures improve long-term security maturity and ensure that the organization can respond effectively to incidents, continuously improve its security, and maintain compliance and resilience, while focusing on practical and cost-effective improvements that can be implemented by a small IT team without significant operational disruption.

---

### 5. Estimated Budget Allocation

The security budget (€80,000 per year) should be allocated across key areas to achieve the greatest risk reduction while staying within financial and operational constraints.
Security tools take around €30,000 of the annual budget. This includes endpoint protection (EDR/antivirus), Microsoft 365 security features (such as Defender and MFA), and basic monitoring and logging tools.
These tools are important because they help protect systems, detect attacks, and respond to threats like malware, ransomware, and phishing.
Even though this is the biggest part of the budget, most of these tools will be implemented in Phase 2 and Phase 3. Phase 1 mainly focuses on low-cost improvements such as policies, basic security setup, and employee training.
Infrastructure improvements take around €20,000 of the annual budget. This includes network segmentation (VLANs and firewall configuration), backup improvements (such as cloud or offline backups), and secure VPN configuration.
These improvements help increase overall system resilience and limit the spread of attacks, especially in production environments.
External consulting takes around €15,000 of the annual budget. This includes support with risk assessment, security policy development, and incident response planning.
Since the internal IT team is small (3 people), external expertise helps implement best practices more efficiently.
Training and awareness take around €10,000 of the annual budget. This includes employee security awareness training, phishing simulations, and basic cybersecurity education programs.
These activities are important because they reduce human-related risks, which are one of the most common causes of security incidents.
Contingency and incident handling take around €5,000 of the annual budget. This includes emergency response costs and small unforeseen security investments.
This budget is important because it provides flexibility to respond quickly to unexpected threats or incidents.


---

### 6. Metrics for Measuring Security Improvement

The following key performance indicators can be used to measure the effectiveness of the implemented security improvements.
1.	Phishing Click Rate
Measures the percentage of employees who click on simulated phishing emails. A lower click rate shows improved employee awareness and reduced risk of credential theft.
2.	Patching compliance
Measures the percentage of systems that are updated with the latest security patches. Higher compliance reduces vulnerabilities and protects against known exploits.
3.	Number of incidents
Tracks the total number of detected security incidents over time. A decrease may indicate improved security, while an increase (initially) may show better detection.
4.	Backup Success Rate
Measures how often backups are completed successfully and can be restored. Ensures the organization can recover data in case of ransomware or system failure.
5.	Mean Time to Detect and Respond (MTTD / MTTR) 
Measures how quickly security incidents are detected and resolved. Faster detection and response reduce damage and downtime.
These key performance indicators should be reviewed regularly (e.g. monthly or quarterly) to ensure continuous improvement.

## Deliverables

Submit:

- Security Improvement Plan (2–4 pages)
- Optional: diagrams or tables

Format:

Markdown or PDF.

---

## Evaluation Criteria

| Criterion | Weight |
|-----------|--------|
| Risk identification | 30% |
| Quality of proposed controls | 30% |
| Practical feasibility | 20% |
| Strategic thinking | 10% |
| Clarity and structure | 10% |

---

## Submission

Submit your work as a **Pull Request** in:

```
homework/submission/<student-id>/
```

---

## Tip

Focus on **realistic improvements** that an organization with limited resources could implement.
Avoid proposing overly complex or expensive solutions.
