# Week2 Of EncryptLabs — AWS Account Hardening & Secure Cloud Security Homelab

**Task ID:** CSE-AWS-L-002-04
**Difficulty:** Intermediate
**Duration:** ~90 minutes (core) / ~4 CPE credits
**Skill Domain:** AWS Cloud Security / IAM / Logging & Monitoring

## 🎯 Objective
Harden an AWS account before deploying workloads — enabling MFA, billing alerts,
least-privilege IAM, full logging/monitoring (CloudTrail, Config, GuardDuty),
and safely deploying intentionally vulnerable labs (CloudGoat, iam-vulnerable)
inside an isolated homelab VPC.

## 📁 Phases
| Phase | Description | Status |
|-------|-------------|--------|
| [A - Account Hardening](./Phase-A_Account-Hardening) | Root MFA + billing alerts | ✅ |
| [B - Network & Monitoring Setup](./Phase-B_Network-Monitoring-Setup) | Homelab VPC, CloudTrail, Config | ✅ |
| [C - IAM Least Privilege](./Phase-C_IAM-Least-Privilege) | IAM groups, password policy, custom policy | ✅ |
| [D - CloudGoat Deployment](./Phase-D_CloudGoat-Deployment) | CloudGoat + iam-vulnerable via Terraform | ✅ |
| [E - Hosted Labs](./Phase-E_Hosted-Labs) | TryHackMe/CloudGoat labs | ⏳ Not completed (premium) |
| [F - Final Report](./Phase-F_Final-Report) | Threat model, risk matrix, CIS mapping | ✅ |

## 🛠️ Tools Used
AWS CLI, AWS Console, Terraform, CloudGoat, iam-vulnerable, Git, Poetry, jq, Claude/ChatGPT

## 🔗 Frameworks Referenced
CIS AWS Foundations Benchmark v1.5, NIST SP 800-53, ISO 27001, OWASP Cloud Top 10, MITRE ATT&CK (T1078, T1087, T1098, T1190, T1552, T1526, T1562)

## 📄 Final Deliverable
See [`Phase-F_Final-Report/AWS_Homelab_Report.pdf`](./Phase-F_Final-Report/AWS_Homelab_Report.pdf)
