# AI Tool and Vendor Review Checklist

**Created by [Prashant Pahwa](https://www.linkedin.com/in/prashant-pahwa-cism/), CISM** | © 2026 | Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

Use this checklist before approving any AI tool, AI feature or AI vendor. It is written for small businesses and independent consultants and takes 15 to 60 minutes depending on the tool.

> This checklist supports a decision. It does not replace legal, privacy or security advice, and it does not guarantee a vendor is safe.

## How to use

1. Start with the **5-minute triage**. If any starred (★) question fails, stop and do not use the tool with Company data until it is resolved.
2. Complete sections A to F. Answer **Yes**, **No**, **N/A** or **Unknown**, and note the evidence (link, document or screenshot).
3. Treat **Unknown** as **No** until the vendor confirms in writing.
4. Use section H to choose an outcome, and record the decision in section I. Add any residual risk to your AI risk register.
5. After approval, work through section G.

---

## Tool details

| Field | Entry |
| --- | --- |
| Tool / feature name | |
| Vendor | |
| Requested by / business owner | |
| Intended use case | |
| Highest data classification involved | Public / Internal / Confidential / Restricted |
| Users / teams | |
| Reviewer and date | |

## 5-minute triage

| # | Question | Result |
| --- | --- | --- |
| T1 ★ | Does the vendor state that our inputs and outputs are **not used to train** its models by default (or can we turn that off) under the plan we will buy? | |
| T2 ★ | Can users sign in with **company accounts, SSO or MFA** (not personal accounts)? | |
| T3 ★ | Does the vendor have a published **privacy policy and terms** that cover business use? | |
| T4 ★ | Is there a clear statement of **where data is stored and for how long**? | |
| T5 | Can an administrator **see and control** who uses the tool? | |
| T6 | Does the vendor publish **security information** (trust page, SOC 2 or ISO 27001 report summary)? | |
| T7 | Can we **delete our data** and close the account? | |
| T8 | Is the tool's purpose clear and **proportionate** to the data it needs? | |

---

## Detailed review

Mark ★ items as required for approval with Confidential or Restricted data.

### A. Data handling and privacy

| # | Question | Evidence to request | Red flag | Yes / No / N/A / Unknown | Notes |
| --- | --- | --- | --- | --- | --- |
| A1 ★ | Are prompts, files and outputs excluded from model training by default or by contract? | Terms, data processing addendum, admin setting | Training on customer data is on by default and cannot be disabled | | |
| A2 ★ | Is the retention period for prompts, outputs and logs stated, and can we shorten it or turn it off? | Retention policy, admin console | Indefinite retention; no deletion option | | |
| A3 | Is the data location (region) stated, and does it meet our client or legal needs? | Trust page, DPA | Unknown or unrestricted data location | | |
| A4 ★ | Is there a signed data processing agreement where personal data is involved? | DPA | Vendor refuses a DPA | | |
| A5 | Are sub-processors listed and are changes notified? | Sub-processor list | No list; no notice of changes | | |
| A6 | Are international transfer mechanisms in place where needed? | DPA, transfer terms | No mechanism for transfers outside your region | | |
| A7 | Can we export and delete our data on request, including from backups within a stated time? | Terms, support confirmation | No deletion process | | |
| A8 | Who at the vendor can access our content (support staff, reviewers)? Is human review of prompts possible? | Policy, terms | Staff or contractors may read content with no controls | | |

### B. Security of the service

| # | Question | Evidence to request | Red flag | Yes / No / N/A / Unknown | Notes |
| --- | --- | --- | --- | --- | --- |
| B1 ★ | SSO and MFA supported for all users? | Documentation, admin settings | Password-only login | | |
| B2 | Role-based access and an admin console to manage users, workspaces and sharing? | Admin demo or docs | Everyone is an admin; no user management | | |
| B3 ★ | Data encrypted in transit and at rest? | Security documentation | Not stated | | |
| B4 | Independent assurance: SOC 2 Type II, ISO 27001 or equivalent report, or recent third-party penetration test summary? | Report, certificate (check scope and date) | None, or scope does not cover the product | | |
| B5 | Audit logs available for admin and user activity, with export? | Documentation | No logs | | |
| B6 | Security incident and breach notification commitment (timeframe, contact)? | Contract, trust page | No commitment | | |
| B7 | Vulnerability disclosure or bug bounty programme? Recent public security incidents handled well? | Website, news search | Hidden or ignored vulnerabilities; unresolved breach | | |
| B8 | Tenant isolation: is our data separated from other customers, including in shared models or vector stores? | Architecture statement | Shared storage with no isolation described | | |

### C. AI-specific safeguards

| # | Question | Evidence to request | Red flag | Yes / No / N/A / Unknown | Notes |
| --- | --- | --- | --- | --- | --- |
| C1 | Does the vendor describe protections against prompt injection and data leakage between users or sessions? | Security documentation, response to questionnaire | No awareness of the risk | | |
| C2 ★ | If the tool can act (send email, edit files, call APIs, run code), can we limit its permissions and require human approval for high-impact actions? | Product settings | Broad access by default; no approval step | | |
| C3 | Are connectors, plugins, extensions and integrations restricted to an approved list, with minimal permissions? | Admin settings | Anyone can connect anything to company accounts | | |
| C4 | Is it clear which underlying models are used and which third parties process data (model providers)? | Documentation | Unknown model or provider chain | | |
| C5 | Are outputs filtered or moderated, and are limits on cost and usage available (rate limits, spend caps)? | Admin settings | No usage controls | | |
| C6 | Does the vendor describe testing for accuracy, bias and safety, and publish known limitations? | Model or system card, documentation | No limitations disclosed | | |
| C7 | If the tool supports retrieval from our documents, are existing document permissions respected (users only retrieve what they may already access)? | Test with two users | The tool exposes documents users should not see | | |
| C8 | Are AI-generated outputs clearly labelled to users where relevant? | Product check | Output presented as fact with no indication | | |

### D. Legal and contractual

| # | Question | Evidence to request | Red flag | Yes / No / N/A / Unknown | Notes |
| --- | --- | --- | --- | --- | --- |
| D1 ★ | Do the terms give us rights to use the outputs commercially? | Terms of service | Vendor claims ownership of outputs or broad licence to our content | | |
| D2 | Is there intellectual property indemnification for output-related claims, and what are its conditions? | Contract | None, or conditions make it unusable | | |
| D3 | Are liability caps and warranties acceptable for the risk of this use? | Contract | Liability limited to a trivial amount for a critical use | | |
| D4 | Does the contract allow us to use the tool with client data under our client contracts? | Client contracts | Client contract forbids AI or third-party processing | | |
| D5 | Does the vendor state its role and obligations under applicable AI rules (for example the EU AI Act) and data protection law? | Vendor statement | Vendor cannot say | | |
| D6 | Can the vendor change terms (including data use) without notice? | Terms | Unilateral change with no notice | | |

### E. Reliability and continuity

| # | Question | Evidence to request | Red flag | Yes / No / N/A / Unknown | Notes |
| --- | --- | --- | --- | --- | --- |
| E1 | Is there a published uptime commitment or status page, with support channels? | Status page, SLA | No support route | | |
| E2 | Can we export our content and configuration to leave (exit plan)? | Documentation | Data locked in | | |
| E3 | Is pricing clear, including usage-based charges and what happens when limits are reached? | Pricing page | Open-ended usage charges | | |
| E4 | Is the vendor financially stable and established, or a new service that may close? | Company information | Very new with no track record, for a critical use | | |
| E5 | What happens when the model or product changes or is retired? | Vendor policy | Frequent silent changes to behaviour | | |

### F. Responsible use and fit

| # | Question | Evidence to request | Red flag | Yes / No / N/A / Unknown | Notes |
| --- | --- | --- | --- | --- | --- |
| F1 | Is the intended use low risk? Not used to make or finalise decisions about people (hiring, credit, pricing, discipline) without human review? | Use case description | Automated decisions about individuals | | |
| F2 | Does the use case involve a regulated area (health, finance, legal advice, critical infrastructure, children)? If yes, has specialist advice been taken? | Use case description | Regulated use with no review | | |
| F3 | Is there a named business owner accountable for the tool, its use and its output? | Register entry | No owner | | |
| F4 | Are users trained on the Acceptable Use Policy before getting access? | Training record | Access granted without training | | |

### G. Monitoring after approval

| # | Question | Done? | Notes |
| --- | --- | --- | --- |
| G1 | Tool added to the approved AI tool register with owner, purpose, data classification and review date | | |
| G2 | Risks from this review added to the AI risk register | | |
| G3 | Settings applied (SSO, MFA, training opt-out, retention, connector restrictions) and a second person checked them | | |
| G4 | Logging or usage reports reviewed on a schedule (at least quarterly) | | |
| G5 | Re-review date set (at least every 12 months, and when the vendor changes terms, models or ownership) | | |

---

## H. Scoring and decision guide

| Outcome | When to use it |
| --- | --- |
| **Approve** | All triage ★ items pass. All ★ items in A to D pass for the data classification involved. No unmitigated red flags. |
| **Approve with conditions** | One or more non-critical items fail but can be controlled (for example restrict to Internal data only, turn off a connector, add MFA). Record each condition and its owner and date. |
| **Reject or pause** | Any triage ★ fails, any ★ item fails for the data involved, or a red flag cannot be mitigated. Reconsider if the vendor changes its position in writing. |

## I. Decision record

| Field | Entry |
| --- | --- |
| Decision | Approve / Approve with conditions / Reject |
| Maximum data classification allowed | Public / Internal / Confidential / Restricted |
| Conditions | |
| Residual risks (reference to risk register IDs) | |
| Approved by (name, role) | |
| Date | |
| Next review date | |

---

## Questions to send a vendor (copy and paste)

1. Do you use our prompts, files or outputs to train or improve models, for you or any third party? Can this be disabled for our account, and is that stated in the contract?
2. How long do you retain prompts, outputs and logs, and how can we delete them?
3. Where is our data stored and processed, and which sub-processors can access it?
4. Which independent security assessments do you hold (for example SOC 2 Type II or ISO 27001), and can you share the report or summary under NDA?
5. How do you protect against prompt injection and against data leaking between customers?
6. If your product takes actions on our behalf, how can we limit its permissions and require approval?
7. What are your breach notification commitments and timeframes?
8. Who owns the outputs, and do you offer indemnification for intellectual property claims?
9. How do we export our data and leave the service?

---

*This checklist was created by Prashant Pahwa and is licensed under CC BY 4.0. Credit the author and link to the licence if you share or adapt it.*
