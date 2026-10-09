# Data Protection Impact Assessment (DPIA) Framework
**Law Nº 058/2021 relating to the Protection of Personal Data and Privacy (Rwanda)**

## 1. Project Information
- **System Name:** Centralized District SACCO Digital Integration & Cooperative Bank Gateway
- **Data Controller:** MINECOFIN / Cooperative Bank Steering Committee
- **Lead Assessor:** Sylvain Imena (Senior Manager – Cybersecurity, Risk & Compliance)

## 2. Description of Processing Operations
- **Categories of Data Subjects:** D-SACCO Members (416 Umurenge SACCOs footprint), Cooperative Bank Customers, System Operators.
- **Personal Data Collected:** National Identification Number (NIN / Indangamuntu), biometrics, telephone number, account balances, physical residential addresses, loan records.
- **Lawful Basis for Processing:** Legal obligation (BNR Banking Regulations), execution of financial contract, public interest under Rwanda Vision 2050 financial inclusion goals.

## 3. Necessity & Proportionality Assessment
- Data minimization implemented at the API Gateway: only transaction amounts and hashed identifiers are passed through clearing rails.
- Storage limitation: Inactive transactional data archived in encrypted tables after statutory audit retention period (10 years).

## 4. Privacy Risk & Mitigation Strategy

| Identified Risk | Impact | Likelihood | Technical / Governance Countermeasure | Residual Risk |
| :--- | :--- | :--- | :--- | :--- |
| Exfiltration of Member National IDs via core banking query dumps | High | Medium | Forcepoint DLP classifiers + Row-Level Security (RLS) on Postgres database clusters | Low |
| Unauthorized employee access to financial statements at branch level | High | High | Role-Based Access Control (RBAC) + Centralized PAM session recording | Low |
| Cross-border data transfer violations without NCSA authorization | Critical | Low | On-premise sovereign data center hosting within Rwanda; zero unauthorized external replication | Low |
