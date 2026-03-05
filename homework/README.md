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

Briefly describe the current security level.

---

### 2. Top 10 Security Risks

Identify and describe the most important cybersecurity risks.

---

### 3. Priority Security Improvements

Propose **10 concrete security improvements**.

Examples:

- policies
- technical controls
- organizational measures
- training programs

Explain **why each measure is important**.

---

### 4. Implementation Roadmap

Create a **12–18 month implementation plan**.

Example phases:

- Phase 1 — Immediate improvements
- Phase 2 — Medium-term improvements
- Phase 3 — Strategic improvements

---

### 5. Estimated Budget Allocation

Provide a rough estimate of how the annual security budget (€80,000) should be used.

Example categories:

- security tools
- training
- external consulting
- infrastructure improvements

---

### 6. Metrics for Measuring Security Improvement

Propose **5 security metrics (KPIs)** that management can use to measure improvement.

Examples:

- phishing click rate
- patching compliance
- number of incidents
- backup success rate

---

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
eng/homework/submission/<student-id>/
```

---

## Tip

Focus on **realistic improvements** that an organization with limited resources could implement.
Avoid proposing overly complex or expensive solutions.