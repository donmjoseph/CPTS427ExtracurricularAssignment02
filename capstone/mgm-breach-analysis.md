# Final Project: Analyzing a Data Breach
## IBM Cybersecurity Case Studies and Capstone Project

---

## Task 1.1 — Case Study Name

**The 2023 MGM Resorts International Cyberattack**

---

## Task 1.2 — Introduction

In September 2023, MGM Resorts International, one of the world's largest hospitality and entertainment companies, fell victim to a sophisticated cyberattack that paralyzed operations across more than 30 properties. The attack was orchestrated by two threat actor groups — Scattered Spider and ALPHV (BlackCat) — who leveraged social engineering to gain initial access before deploying ransomware across MGM's critical infrastructure. Within ten minutes of a vishing call to MGM's IT help desk, attackers obtained administrator-level credentials and infiltrated the company's Okta and Azure environments. The resulting disruption took down slot machines, digital room keys, ATMs, online reservations, and payment systems for nearly ten days. MGM refused to pay the ransom, ultimately absorbing an estimated $100 million in losses. This case study presents critical lessons in identity verification, incident response, and the human element of cybersecurity.

---

## Task 2 — Citations

Kovacs, E. (2023, September 14). Ransomware gang takes credit for disruptive MGM Resorts cyberattack. *SecurityWeek*. https://www.securityweek.com/ransomware-gang-takes-credit-for-highly-disruptive-mgm-resorts-attack/

Toulas, B. (2023, October 5). MGM Resorts ransomware attack led to $100 million loss, data theft. *BleepingComputer*. https://www.bleepingcomputer.com/news/security/mgm-resorts-ransomware-attack-led-to-100-million-loss-data-theft/

---

## Task 3 — Case Study Analysis Template

### 3.1 — Root Causes

**Root Cause 1: Weak help desk identity verification protocols**

Scattered Spider exploited the absence of strong caller authentication at MGM's IT service desk. By finding an employee on LinkedIn and impersonating them over a ten-minute phone call, attackers obtained administrator credentials without any meaningful verification challenge.

**Root Cause 2: Inadequate network segmentation and MFA controls**

Once inside, attackers escalated privileges across MGM's Okta and Azure environments with limited resistance. Weak multi-factor authentication and poor network segmentation allowed them to move laterally and deploy ransomware to over 100 ESXi hypervisors.

---

### 3.2 — Actions Taken

**Action 1: Emergency system shutdown**

Upon detecting unusual activity on September 9, MGM's security team deactivated Okta Sync servers and shut down critical infrastructure components to prevent further escalation. This included taking down reservation systems, digital keys, and payment terminals.

**Action 2: Engagement of external cybersecurity firms and law enforcement**

MGM immediately brought in third-party incident response firms and notified federal authorities. They chose not to pay the ransom and worked with investigators to restore systems, achieving full operational recovery by September 19, 2023.

---

### 3.3 — Effectiveness and Timeliness of Actions

**Action 1 — Emergency system shutdown:** Partially effective. While it stopped further lateral movement, the shutdown itself caused massive operational disruption and ALPHV was still able to deploy ransomware to over 100 ESXi hypervisors before full containment was achieved. The response was reactive rather than proactive.

**Action 2 — External firm engagement and law enforcement:** Effective in the long term. Full operations were restored within ten days, and MGM's refusal to pay the ransom is considered a sound decision by cybersecurity experts. However, the prolonged recovery timeline suggests incident response playbooks were underprepared before the attack occurred.

---

### 3.4 — Successes, Gaps, and Failures

**Success:** MGM refused to pay the ransom and successfully restored full operations within ten days through coordination with external cybersecurity firms and law enforcement, avoiding the precedent-setting mistake made by Caesars Entertainment, which paid approximately $15 million.

**Gap:** There was no robust identity verification process at the IT help desk. The absence of phishing-resistant MFA and caller authentication made it trivially easy for attackers to impersonate an employee and gain elevated privileges.

**Failure:** MGM's incident response playbooks were inadequate for the scale of the attack. ALPHV publicly noted that MGM implemented "conditional restrictions due to inadequate administrative capabilities and weak incident response playbooks," indicating the organization was caught unprepared despite having experienced a breach in 2019.

---

### 3.5 — Impact on the Organization

**Impact 1: Short-term financial and operational impact**

MGM reported an estimated $100 million loss in its third-quarter 2023 results, with daily revenue losses of approximately $8.4 million during peak disruption. Guests across 30+ properties were unable to use digital keys, ATMs, slot machines, or online booking systems, severely damaging customer experience and brand trust.

**Impact 2: Long-term legal and reputational impact**

MGM faced multiple class-action lawsuits and regulatory investigations following the breach. By 2025, MGM launched a settlement program covering both the 2019 and 2023 breaches. The company also committed to investing $40 million in additional cybersecurity safeguards, signaling a long-term financial obligation stemming from the incident.

---

### 3.6 — Lessons Learned

**Lesson 1: The human element is the most exploitable attack surface**

The entire breach originated from a single phone call. No amount of technical security infrastructure matters if social engineering can bypass it at the help desk level. Organizations must invest in rigorous caller verification protocols and employee awareness training.

**Lesson 2: Incident response plans must be tested and current**

MGM had previously experienced a breach in 2019 yet still lacked adequate incident response playbooks in 2023. Regular tabletop exercises and updated IR plans are essential to ensure swift, coordinated containment when an attack occurs.

---

### 3.7 — Recommendations for Future Actions

**Recommendation 1: Implement phishing-resistant MFA and zero-trust identity verification at all service desks**

Help desk staff should be required to verify callers through out-of-band authentication methods — such as push notifications to registered devices or hardware tokens — before granting any account access. This directly addresses the initial attack vector.

**Recommendation 2: Conduct regular red team exercises focusing on social engineering scenarios**

Organizations should simulate vishing and impersonation attacks against their own help desks to identify weaknesses before adversaries do. These exercises should be documented, reviewed, and used to update IR playbooks on a recurring basis.

---

### 3.8 — Conclusion`

The 2023 MGM Resorts cyberattack is a defining case study in modern cybersecurity because it demonstrates that even large, well-resourced organizations remain vulnerable when human factors are overlooked. A ten-minute phone call bypassed billions of dollars worth of technical infrastructure. The attack highlights a broader industry trend: threat actors are increasingly targeting the human layer — help desks, employees, and identity systems — rather than attempting to crack hardened technical defenses directly. For the hospitality and gaming sector, which relies heavily on interconnected digital systems, the implications are severe. The long-term consequences — lawsuits, regulatory scrutiny, reputational damage, and a $40 million security investment — underscore that proactive cybersecurity investment is always cheaper than reactive recovery. Organizations across all industries should treat this case as a blueprint for what not to do, and use it to harden their identity verification, network segmentation, and incident response capabilities before an attack occurs.

**References:**

Kovacs, E. (2023, September 14). Ransomware gang takes credit for disruptive MGM Resorts cyberattack. *SecurityWeek*. https://www.securityweek.com/ransomware-gang-takes-credit-for-highly-disruptive-mgm-resorts-attack/

Toulas, B. (2023, October 5). MGM Resorts ransomware attack led to $100 million loss, data theft. *BleepingComputer*. https://www.bleepingcomputer.com/news/security/mgm-resorts-ransomware-attack-led-to-100-million-loss-data-theft/
