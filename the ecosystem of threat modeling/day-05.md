![Banner](../images/banner.jpg)

hello again!! 
today's task is to write a Threat Model report for a fictional AI customer-support bot
i never wrote a report for such purpose in my entire life, i guess it would be nice to understand and see how threat modelers write thier reports 

# Threat Model Report
## SupportBot - AI Customer-Support System

**Prepared for:** SupportAI Leadership Team
**Prepared by:** NAUR
**Date:** 08/08/2026
**Version:** 1.0

---

## 1. Executive Summary

[Brief overview of the system and key findings]

### Key Findings

| # | Finding | Severity |
|---|---------|----------|
| 1 | [Finding] | [Critical/High/Medium/Low] |
| 2 | [Finding] | [Critical/High/Medium/Low] |
| 3 | [Finding] | [Critical/High/Medium/Low] |

### Recommendations

1. [Most critical fix]
2. [Second most critical fix]
3. [Other fixes]

---

## 2. System Overview

### 2.1 Purpose
SupportBot is an AI-powered customer support automation system.

### 2.2 Components
| Component | Description |
|-----------|-------------|
| Knowledge Base | Customer's internal documents, FAQs, policies |
| Vector Database | Pinecone for storing document embeddings |
| LLM | Groq API for generating responses |
| CRM Integration | Salesforce for ticket creation |
| Web Interface | Customer-facing chat interface |

### 2.3 Data Flow
1. Customer asks a question via web chat
2. SupportBot converts question to vector
3. Vector database retrieves relevant documents
4. LLM generates response based on retrieved context
5. Response is sent to customer
6. If needed, a ticket is created in Salesforce

---

## 3. Assets Identified

| Asset | Description | Value | Sensitivity |
|-------|-------------|-------|-------------|
| Customer PII | Names, emails, phone numbers | High | Critical |
| Internal Documents | Company policies, procedures | High | Confidential |
| Customer Data | Customer-specific information | High | Critical |
| API Keys | Groq, Pinecone, Salesforce | High | Critical |
| Vector Database | All documents + embeddings | High | Confidential |
| LLM Access | Ability to generate responses | Medium | Internal |

---

## 4. STRIDE Threat Analysis

### S - Spoofing

| Threat | Description | Likelihood | Impact | Severity |
|--------|-------------|------------|--------|----------|
| [Threat] | [Description] | [High/Med/Low] | [High/Med/Low] | [Critical/High] |

### T - Tampering

| Threat | Description | Likelihood | Impact | Severity |
|--------|-------------|------------|--------|----------|
| [Threat] | [Description] | [High/Med/Low] | [High/Med/Low] | [Critical/High] |

### R - Repudiation

| Threat | Description | Likelihood | Impact | Severity |
|--------|-------------|------------|--------|----------|
| [Threat] | [Description] | [High/Med/Low] | [High/Med/Low] | [Critical/High] |

### I - Information Disclosure

| Threat | Description | Likelihood | Impact | Severity |
|--------|-------------|------------|--------|----------|
| [Threat] | [Description] | [High/Med/Low] | [High/Med/Low] | [Critical/High] |

### D - Denial of Service

| Threat | Description | Likelihood | Impact | Severity |
|--------|-------------|------------|--------|----------|
| [Threat] | [Description] | [High/Med/Low] | [High/Med/Low] | [Critical/High] |

### E - Elevation of Privilege

| Threat | Description | Likelihood | Impact | Severity |
|--------|-------------|------------|--------|----------|
| [Threat] | [Description] | [High/Med/Low] | [High/Med/Low] | [Critical/High] |

---

## 5. Detailed Threat Descriptions

### 5.1 [Threat Name]

| Attribute | Details |
|-----------|---------|
| **Category** | [S/T/R/I/D/E] |
| **Asset** | [Affected asset] |
| **Description** | [Detailed description] |
| **Attack Vector** | [How the attack happens] |
| **Impact** | [What happens if exploited] |
| **Likelihood** | [High/Med/Low] |
| **Severity** | [Critical/High/Medium/Low] |

**Example Scenario:**
[Realistic attack scenario]

**Mitigation:**
[How to fix it]

---

## 6. Attack Scenarios

### Scenario 1: [Name of Attack]

**Attacker:** [Who is the attacker?]
**Goal:** [What are they trying to achieve?]
**Method:** [How do they do it?]
**Impact:** [What happens?]

**Step-by-Step:**
1. [Step 1]
2. [Step 2]
3. [Step 3]

**Mitigation:**
[How to prevent this attack]

### Scenario 2: [Name of Attack]
...

### Scenario 3: [Name of Attack]
...

---

## 7. Mitigations Summary

| # | Threat | Mitigation | Priority | Status |
|---|--------|------------|----------|--------|
| 1 | [Threat] | [Mitigation] | Critical | Not Implemented |
| 2 | [Threat] | [Mitigation] | High | Partially Implemented |
| 3 | [Threat] | [Mitigation] | Medium | Implemented |

### Detailed Mitigations

| Mitigation | Description | Implementation Cost | Timeline |
|------------|-------------|---------------------|----------|
| [Mitigation] | [Description] | [High/Med/Low] | [Timeframe] |

---

## 8. Priority Order

### Critical (Fix Immediately)
1. [Critical issue 1]
2. [Critical issue 2]

### High (Fix Soon)
1. [High issue 1]
2. [High issue 2]

### Medium (Plan for Fix)
1. [Medium issue 1]
2. [Medium issue 2]

### Low (Monitor)
1. [Low issue 1]
2. [Low issue 2]

---

## 9. Conclusion

### Key Takeaways
- [Key takeaway 1]
- [Key takeaway 2]
- [Key takeaway 3]

### Next Steps
1. [Action item 1]
2. [Action item 2]
3. [Action item 3]

---

## 10. Appendix

### A. STRIDE Reference
- **S** - Spoofing: Impersonating someone else
- **T** - Tampering: Modifying data without permission
- **R** - Repudiation: Denying actions
- **I** - Information Disclosure: Exposing sensitive data
- **D** - Denial of Service: Making system unavailable
- **E** - Elevation of Privilege: Getting unauthorized access

### B. References
- [Any resources used]
- [OWASP Top 10 for LLMs]
- [MITRE ATLAS]