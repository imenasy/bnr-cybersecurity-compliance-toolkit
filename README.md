markdown
# BNR Cybersecurity Directives & GRC Audit Toolkit

A complete Governance, Risk, and Compliance (GRC) framework operationalizing National Bank of Rwanda (BNR) regulations, Law Nº 058/2021 on Personal Data Protection, and ISO/IEC 27001:2022 controls for District SACCOs.

## Contained Tools
- **BNR Compliance Audit Checklist:** 84 controls covering boundary defense, data protection, and incident reporting.
- **Enterprise IT Risk Register:** Quantitative and qualitative scoring (ISO 31000) for core banking systems.
- **Data Protection Impact Assessment (DPIA):** Tailored for cooperative banking operations.



*risk/it_risk_register_iso31000.csv*:

csv
Risk_ID,Asset_Category,Threat_Vulnerability,Inherent_Risk,Mitigation_Control,Residual_Risk,Owner,Monitoring_Frequency
RSK-001,Payment Switch,Unauthorized RIPPS/RNDPS switch transaction injection via API,High (16),Enforce mTLS + HSM payload signing + anomalous velocity limits,Low (4),Senior Manager CyberSec,Real-Time (SOC)
RSK-002,CBS Database,Direct SQL balance alteration by privileged user,Critical (20),LogRhythm DB auditing + PAM session recording + dual authorization,Medium (6),Senior Manager CyberSec,Daily Audit
RSK-003,District SACCO Endpoint,Ransomware propagation across branch WAN/VPN,High (15),CrowdStrike Falcon EDR + microsegmentation + automated isolation,Low (3),SOC Lead,Continuous



---
