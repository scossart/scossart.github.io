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

### 1. Okta Group Rules & Manual Membership Audit

**Goal:** Detect users who were manually added to groups that are supposed to be fully driven by Group Rules.

**What it does:**

- Retrieves Okta group rules and their conditions (attributes, group membership, etc.)
- Builds the expected membership set for each rule-based group
- Compares it with the actual group members
- Detects:
  - users present in the group but not matching the rule conditions
  - potential inconsistencies between rules and real life
- Exports results to Excel (XLSX) for IAM / security review

**Tech stack:** Python, Okta REST API, JSON, Excel export.

_Status:_ Already working in my environment; public version to be cleaned and pushed.

---

### 2. Okta Group & Rule Renaming Automation

**Goal:** Help rename groups and their associated rules safely and consistently at scale.

**What it does:**

- Reads Okta groups and their associated rules
- Applies controlled rename patterns (e.g. replacing a specific keyword)
- Updates:
  - group names
  - rule names
  - rule conditions where needed (string replacements inside expressions)
- Logs each change for review and rollback if necessary

**Tech stack:** Python, Okta REST API, JSON deep copy / manipulation.

_Status:_ Script already in use; being refactored for public release with sanitized examples.

---

### 3. Entra ID (Azure AD) Audit Scripts *(planned)*

**Goal:** Build a small toolkit to audit core Entra ID security configuration.

Planned modules:

- MFA status report per user
- Sign-in logs extraction and basic anomaly detection (locations, IP changes, failure spikes)
- Inactive account detection based on sign-in and/or last password change
- Export to CSV / Excel for follow-up actions

**Tech stack:** Python or PowerShell, Microsoft Graph API.

_Status:_ Design phase; will be built progressively and published module by module._

---

### 4. Identity-as-Code Lab *(planned)*

**Goal:** Prove that a small Okta / Entra configuration can be described, versioned and recreated from code.

Planned scope:

- A minimal set of:
  - groups
  - apps
  - policies (MFA, sign-on)
- Managed via Terraform or Python scripts
- Ability to:
  - recreate a sandbox
  - track configuration changes over time
  - review changes like code (pull requests, diffs)

**Tech stack:** Terraform (if relevant provider), Python, Git.

_Status:_ Early design. This will be one of my main focus areas going forward._

---

## What I’m building next

Short-term focus:

- Clean and open-source my existing Okta automation scripts (audit, rename, consistency checks)
- Build small but **realistic labs** for:
  - CIAM security scenarios (brute force, account recovery flows)
  - OAuth2 / OIDC flows with a demo app
- Move toward a more **Identity-as-Code** approach:
  - less manual click-ops
  - more reproducible configurations

As my professional experience grows (especially around CIAM), this portfolio will evolve to reflect more advanced architectures and real-world patterns.

---

## Contact

- **GitHub:** `scossart`  
- **Email:** `samuel.cossart1@gmail.com`  

If you work on IAM / CIAM, automation or cloud security and want to discuss ideas, I’m always open to connect.
