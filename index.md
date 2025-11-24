---
title: "Jean Michel – IAM & CIAM Engineer"
---

# Samuel Cossart – IAM & CIAM Consultant
**Okta · Entra ID · Identity Automation**

---

## About me

I’m an Identity & Access Management engineer focused on **cloud IAM, CIAM and automation**.

My goals are simple and very pragmatic:

- Build and operate **secure, resilient identity platforms**
- Replace repetitive admin work with **code and automation**
- Make IAM configurations **observable, auditable and reproducible**
- Strong experience with the Microsoft ecosystem (Azure, Entra ID, Active Directory), which helps me bridge traditional infrastructure with modern cloud IAM practices.

I currently work as a systems / IAM administrator in a large retail environment, handling day-to-day identity operations, troubleshooting and continuous improvement around workforce identity.  
This portfolio is the technical side of my work: scripts, tools, and labs that show how I think and build.

---

## Core skills

### Identity & Access Management

- Okta Workforce: groups, group rules, app assignments, MFA policies, sign-on policies
- Microsoft Entra ID (Azure AD): Conditional Access, security defaults, user lifecycle basics
- Authentication and federation: SAML 2.0, OAuth 2.0, OpenID Connect (concepts & flows)
- Group and attribute modelling for large user populations
- Basic CIAM concepts: account recovery, brute-force protection, friction vs security trade-offs

### Automation & Identity-as-Code

- **Python** for:
  - Okta and Entra ID REST API integration
  - Bulk operations (create/update groups, users, rules)
  - Auditing and reporting (CSV / Excel exports)
- PowerShell for Entra ID and Microsoft 365
- JSON / YAML for config, templates and rule definitions
- First steps with **Terraform** for identity resources (planned & in progress)

### Cloud & Security Mindset

- Understanding of cloud IAM patterns (central identity, SSO, MFA everywhere)
- Least privilege, conditional access, network zones, IP filtering
- Audit mindset: logs, traces, “what happened / who did what / why”

### Microsoft Ecosystem Integration

- Entra ID (Azure AD): Conditional Access, MFA, identity governance basics
- Azure infrastructure basics (subscriptions, networking, identity services)
- Active Directory & hybrid identity (sync concepts, authentication flows)
- PowerShell automation for identity and M365 workflows

---

## Selected projects

> ⚠️ This is a **first version** of the portfolio. Some projects are already in code privately and will be progressively documented and published.

### **1. Tenant-wide MFA rollout (Okta Workforce)**  
**Goal:** Deploy strong authentication across the entire organization (~3,000+ users) with minimal friction and full business continuity.

**What I did:**
- Designed and deployed **MFA enrollment flows** for all workforce users  
- Managed communication, onboarding plans and exception paths  
- Implemented MFA policies based on:
  - group membership  
  - network zones  
  - device trust  
- Ensured compatibility with existing SSO apps and legacy authentication  
- Provided support, troubleshooting and fine-tuning during rollout  
- Reduced friction while maintaining strong security requirements  

**Impact:** The company migrated from weak authentication to **full MFA coverage** across critical applications.

**Tech stack:** Okta policies, network zones, enrollment flows, user lifecycle coordination.

---

### **2. SSO & automatic provisioning for 100+ applications**

**Goal:** Centralize authentication and automate user provisioning for a large application portfolio.

**What I did:**
- Integrated more than **100 internal and third-party applications** into Okta  
- Implemented SSO using SAML 2.0, OIDC and WS-Fed depending on vendor capabilities  
- Built provisioning workflows:
  - SCIM 2.0  
  - API-based provisioning  
  - group-based assignments  
- Collaborated with application owners to validate mappings, roles and lifecycle logic  
- Ensured clean deprovisioning and access revocation  
- Maintained documentation and onboarding procedures for new apps

**Impact:** Strong reduction in manual work, consistent access controls, faster onboarding and improved security across the application landscape.

**Tech stack:** Okta SSO (SAML/OIDC), SCIM provisioning, API connectivity, attribute mapping.

---

### **3. Okta Group Rules: audit, cleanup & automation (Python)**

**Goal:** Ensure consistency between **Okta Group Rules**, actual group memberships, and naming conventions.

**What I built:**
- Script to extract and analyze all Okta Group Rules (conditions, expressions, source groups)  
- Logic to rebuild the **expected membership set** for each rule  
- Comparison engine to detect:
  - users manually added to rule-driven groups  
  - inconsistent rule conditions  
  - drift between rules and reality  
- Automated cleanup options with Excel export for IAM teams  
- Safe renaming system for groups & rules:
  - controlled keyword replacements  
  - expression updates inside rule conditions  
  - full logging for rollbacks

**Impact:** Improved rule reliability, reduced manual discrepancies, and created a foundation for future Identity-as-Code adoption.

**Tech stack:** Python, Okta REST API, JSON deep-copy manipulation, Excel export.

**Status:** Already running in production; public version being sanitized and refactored.

---

### **4. Entra ID (Azure AD) audit toolkit *(planned)***

**Goal:** Provide automated visibility and reports on core Entra ID security posture.

**Planned modules:**
- MFA status report per user  
- Sign-in logs extraction + anomaly detection (IP changes, geo shifts, failure bursts)  
- Inactive accounts detection  
- License audit and user lifecycle checks  
- Export to CSV / Excel for review and actions

**Tech stack:** Python or PowerShell, Microsoft Graph API.

**Status:** Design phase; modules will be published progressively.

---

### **5. Identity-as-Code (Okta & Entra) *(planned)***

**Goal:** Demonstrate that identity configurations can be managed like code and fully reconstructed.

**Planned scope:**
- Minimal reproducible environment:
  - core groups  
  - MFA & sign-on policies  
  - sample applications  
- Versioned configuration using Terraform (or Python templates)  
- Capable of:
  - sandbox recreation  
  - tracking configuration changes  
  - reviewing diffs via pull requests  
  - automated validation

**Tech stack:** Terraform (if provider relevant), Python, Git.

**Status:** Early research; target project for 2025.

---

## Contact

- **GitHub:** `scossart`  
- **Email:** `samuel.cossart1@gmail.com`  

If you work on IAM / CIAM, automation or cloud security and want to discuss ideas, I’m always open to connect.
