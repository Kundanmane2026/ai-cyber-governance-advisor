# Risk Translation Guide

Turn technical findings into statements a board or executive can weigh against other business risks. Keep the 5×5 scale from `cyber-risk-advisory` so ratings match the risk register.

## 1. The translation pattern

**Event → business service → consequence → likelihood → cost range → what reduces it**

| Technical finding | Business translation |
|---|---|
| "No MFA on VPN; 40% of endpoints lack EDR." | "A single stolen password could let an attacker into our network and lock our core systems. A ransomware outage of 3–7 days would stop [service], cost roughly ₹[x–y] crore, and require reports to CERT-In within 6 hours and to [regulator]. Enforcing MFA and completing EDR roll-out (₹[z] lakh, 60 days) cuts this likelihood from Likely to Unlikely." |
| "Logs kept 30 days, on a foreign cloud region." | "We cannot meet CERT-In's requirement to keep 180 days of logs in India, and after an incident we may not be able to show what happened. This exposes us to regulatory action and weakens any legal case." |
| "Personal data of 2 lakh customers in an unencrypted test database." | "A copy of real customer data sits in a less-protected test system. If exposed, we must notify the Data Protection Board and every affected customer, and face a penalty that can reach ₹250 crore under the DPDP Act Schedule for failing to protect data." |
| "Chatbot can call internal APIs without approval." | "Our customer chatbot can take actions in internal systems with no human check. A manipulated conversation could trigger wrong refunds or disclose data. Adding approval steps and narrowing its permissions removes most of this risk." |
| "Vendor contract has no breach-notice clause." | "If our IT vendor is breached, nothing obliges them to tell us in time for our own 6-hour CERT-In report." |

Rules:
- One sentence for the risk, one for the cost, one for the fix.
- Name the business service, not the server.
- Say who is harmed (customers, the company, staff, the public).
- Replace "critical vulnerability" with what could happen and how likely it is.

## 2. Loss-range method (three-point estimate)

Use ranges, never a single figure. Label each input.

| Component | How to estimate | Typical source |
|---|---|---|
| Business interruption | Revenue or margin per hour of critical service × outage hours (low / likely / high) | Finance; BIA |
| Response and recovery | Forensics, legal, IR retainer, overtime, rebuild | Quotes; insurer panel rates |
| Notification and customer remediation | Number of affected people × cost per notice, helpline, credit monitoring | Operations |
| Regulatory exposure | Penalty band under the applicable schedule (DPDP Schedule; sector regulator; GDPR if triggered) — give the band, never a prediction | Statute; counsel |
| Litigation and compensation | Claims under IT Act s.43A (while in force) / contract / consumer law | Counsel |
| Contract and revenue loss | Customer churn, SLA credits, lost tenders | Sales; contracts |
| Reputation | Qualitative unless market data exists | Comms |

**Present as:** "Likely loss ₹[x] crore (range ₹[low]–₹[high]), driven mainly by [component]." Note insurance cover and its notification conditions separately. Methods such as FAIR may be used for deeper quantification; state the method used.

## 3. Business case template

1. **Problem** (2 lines, business language).
2. **Current exposure:** rating and loss range (with labels).
3. **Options table:**

| Option | One-time cost | Annual cost | Residual rating | Regulatory position | Time to value | Dependencies |
|---|---|---|---|---|---|---|
| A. Do nothing | 0 | 0 | | | — | |
| B. Minimum compliance | | | | | | |
| C. Recommended | | | | | | |
| D. Best-in-class | | | | | | |

4. **Recommendation** and reasoning.
5. **Benefits beyond risk reduction:** audit closure, certification, customer and tender requirements, insurance terms, speed of sale.
6. **Delivery plan summary** and milestones.
7. **Risks of the investment** (adoption, vendor lock-in, skills).
8. **Ask:** amount, approver, date.

## 4. Plain-language glossary (use in annexes)

| Term | Plain gloss |
|---|---|
| Risk appetite | How much risk of a kind we are willing to carry to achieve our goals |
| Inherent / residual risk | Risk before / after counting the controls we can show are working |
| KRI | An early-warning number that shows whether a risk is growing |
| MFA | A second check, beyond a password, before someone can log in |
| EDR | Software on each computer that spots and stops suspicious activity |
| Ransomware | Malicious software that locks our data and demands payment |
| Data Fiduciary | Under the DPDP Act, the organisation that decides why and how personal data is used |
| Significant Data Fiduciary | A Data Fiduciary the government designates for extra duties because of the volume or sensitivity of its data |
| Personal data breach | Any unauthorised use, sharing, loss or alteration of personal data |
| CERT-In | India's national agency for cyber incident response; certain incidents must be reported to it within 6 hours |
| VAPT | Authorised testing to find security weaknesses before attackers do |
| High-risk AI system | Under the EU AI Act, AI used in areas such as credit, hiring or essential services, carrying strict duties |
| RTO / RPO | How fast a service must be back / how much data we can afford to lose |
