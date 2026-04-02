# Security Improvement Plan — GreenFields Food Processing Ltd.

## 1. Security Maturity Assessment

At the moment, GreenFields is at a relatively low level of cybersecurity maturity. Security is lacking basics, which means there are no clear guidelines on how to respond and act.

There are no written policies, risk assessment and responsibilities are not clearly assigned. Comapny wouldn't even know if it was attacked until it would be too late and even then they wouldn't know what to do. If any security is done, it's on ad-hoc basis.

---

## 2. Top 10 Security Risks

1. One main network with production on same LAN   
2. Shared administrator accounts   
3. No monitoring / logging of activity  
4. Backups on the same network   
5. No response plan  
6. UntraINED employees   
7. Inconsistent patching of systems  
8. Questionable VPN security  
9. Unprotected endpoints  
10. No risk assessment process  

---

## 3. Priority Security Improvements

### 1. Network Segmentation
The network should be split into separate segments (production, corporate, guest) using VLANs and firewalls.

**Why:** If an attacker gains access to one part of the network they should not be able to reach other sectors.

---

### 2. Individual Administrator Accounts
Remove shared admin accounts and assign individual accounts with specific permissions.

**Why:** Greatly improves logging and provides overwiev of actions.

---

### 3. Multi Factor Authentication 
Enable MFA for Microsoft 365, VPN access and especially administrator accounts.

**Why:** Obvious MFA pluses, harder to gain access to account.

---

### 4. Endpoint Protection (EDR)
Deploy a centralized endpoint protection solution such as Microsoft Defender.

**Why:** Provides better detection and response capabilities.

---

### 5. Improved Backup Strategy (3-2-1 Rule)
Implement backups that are stored offsite and offline .

**Why:** Provides recovery points if attack happenss.

---

### 6. Security Awareness Training
Introduce basic employee training and phishing simulations.

**Why:** The company already had a phishing incident so human error is a clear weakness

---

### 7. Automated Patch Management
Set up automated updates for operating systems and applications.

**Why:** Many attacks exploit vulnerabilities that could have be patched.

---

### 8. Centralized Logging and Monitoring
Introduce basic logging solution.

**Why:** Makes it easier to detect and investigate incidents.

---

### 9. Device Protection
Enable disk encryption and mobile device management.

**Why:** Protects sensitive data in case devices are lost or stolen.

---

### 10. Incident Response Plan
Create a simple incident response plan with defined steps and responsibilities.

**Why:** Helps organization respond faster and more effectively.

---

## 4. Implementation Roadmap

### Phase 1 (0–3 months) — Immediate Improvements

- Implement network segmentation
- Enable MFA
- Remove shared passwords
- Start employee training

---

### Phase 2 (3–9 months) — Mid term Improvements

- Improve backup strategy
- Deploy endpoint protection
- Automate patch management
- Set up basic logging

---

### Phase 3 (9–18 months) — Strategic Improvements

- Develop and test incident response plan
- Improve monitoring capabilities
- Conduct formal risk assessment
- Continue training programs

---

## 5. Budget Allocation (€80,000/year)

- Security tools (EDR, physical MFA, backups): €30,000    
- Training and awareness: €10,000  
- Infrastructure improvements: €30,000  
- Consulting: €10,000  

---

## 6. Security Metrics (KPIs)

1. Phishing click rate   
2. Patch compliance >95%  
3. Compromissed devices <1  
4. Backup success rate = 100%  
5. Time to detect and respond to incidents <10min  
