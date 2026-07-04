# OMEGA-2 Export Samples

These samples describe the official demonstration export shapes. Runtime export endpoints continue to use existing AEGIS APIs and audit package payloads.

## AI Inventory Export

```csv
agent_id,name,business_unit,department,business_owner,technical_owner,risk,lifecycle,compliance,next_review
AGT-000001,Customer Support Assistant,Customer Success,Support Operations,manager.support@aegisglobal.example,ml.platform@aegisglobal.example,MEDIUM,Monitoring,Compliant,2026-08-01
AGT-000009,Financial Risk Predictor,Finance,Financial Planning and Analysis,manager.fpa@aegisglobal.example,ml.platform@aegisglobal.example,CRITICAL,Monitoring,Exception approved,2026-07-10
AGT-000017,Threat Detection Engine,Cybersecurity,Threat Detection,manager.threat@aegisglobal.example,security.engineering@aegisglobal.example,CRITICAL,Monitoring,Exception approved,2026-07-12
```

## Governance Export

```csv
policy_id,policy_name,owner,control_count,linked_ai_systems,evidence_status,approval_status
RAI-001,Human Oversight Standard,grace.kim@aegisglobal.example,3,critical_and_high_risk_ai,complete,approved
AIG-002,AI Registration and Ownership Policy,grace.kim@aegisglobal.example,3,64,complete,approved
EVD-015,Evidence Retention and Audit Policy,grace.kim@aegisglobal.example,3,64,complete,approved
```

## Risk Register Export

```csv
risk_id,ai_system,severity,probability,impact,owner,mitigation,status
OMEGA2-RISK-AGT-000009,Financial Risk Predictor,CRITICAL,Medium,Enterprise,manager.fpa@aegisglobal.example,Human approval and runtime monitoring,Accepted with mitigation
OMEGA2-RISK-AGT-000017,Threat Detection Engine,CRITICAL,High,Enterprise,manager.threat@aegisglobal.example,Security review and capability restriction,Pending mitigation review
OMEGA2-RISK-AGT-000041,Contract Analysis AI,CRITICAL,Medium,Enterprise,manager.contracts@aegisglobal.example,Legal approval and evidence refresh,Accepted with mitigation
```

## Demo Account Export

```csv
persona,name,email,role,password
CEO,Elena Marquez,elena.marquez@aegisglobal.example,Super Admin,Aegis-Omega2-Demo-2026!
CTO,Marcus Chen,marcus.chen@aegisglobal.example,AI Administrator,Aegis-Omega2-Demo-2026!
CISO,Nadia Okafor,nadia.okafor@aegisglobal.example,Security Administrator,Aegis-Omega2-Demo-2026!
Chief Compliance Officer,Grace Kim,grace.kim@aegisglobal.example,Compliance Officer,Aegis-Omega2-Demo-2026!
Chief AI Officer,Priya Raman,priya.raman@aegisglobal.example,AI Administrator,Aegis-Omega2-Demo-2026!
```

