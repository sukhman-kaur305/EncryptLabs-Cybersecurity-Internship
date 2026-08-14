# ☁️ Week 4 – Cloud Threat Modeling & Attack Surface Identification in AWS

## Junior Cloud Security Engineer Internship | EncryptEdge Labs

This Week 4 project focused on identifying and assessing cloud security risks in a deliberately vulnerable AWS environment.

The lab combined AWS resource enumeration, cloud threat modeling, attack-surface analysis, MITRE ATT&CK mapping, and risk assessment to understand how IAM permissions and cloud misconfigurations can create potential attack paths.

---

## 🎯 Objectives

The main objectives of this project were to:

- Understand cloud threat modeling using STRIDE
- Map AWS security risks to MITRE ATT&CK
- Deploy an intentionally vulnerable AWS environment using CloudGoat
- Enumerate AWS resources using AWS CLI
- Identify potential cloud attack surfaces
- Analyze IAM privilege-escalation risks
- Assess EC2 and S3 exposure
- Build a cloud threat model
- Develop a likelihood × impact risk matrix
- Recommend appropriate security controls

---

## 🛠️ Tools & Technologies

- Amazon Web Services (AWS)
- AWS CLI
- AWS CloudShell
- AWS IAM
- Amazon EC2
- Amazon S3
- CloudGoat
- Terraform
- Threat Dragon
- STRIDE Threat Modeling
- MITRE ATT&CK
- Microsoft Excel

---

## 🔐 Authorized Lab Environment

All activities were performed within an authorized AWS training environment.

The CloudGoat `iam_privesc_by_rollback` scenario was deployed in a personal AWS lab account as an intentionally vulnerable environment.

No production systems, external AWS accounts, third-party cloud resources, or real customer data were accessed.

---

# Phase A – Cloud Threat Modeling

The first phase focused on understanding the fundamentals of cloud threat modeling.

I reviewed the six STRIDE categories:

- **Spoofing** – misuse of stolen or compromised credentials
- **Tampering** – unauthorized modification of resources or policies
- **Repudiation** – activity occurring without sufficient auditability
- **Information Disclosure** – unauthorized exposure of cloud data
- **Denial of Service** – disruption of cloud resources
- **Elevation of Privilege** – gaining higher privileges through insecure IAM configurations

I then created a Threat Dragon diagram showing relationships between:

AWS User → IAM → EC2 → S3

The model helped visualize trust relationships, possible threats, and attack paths.

---

# Phase B – CloudGoat Environment Deployment

CloudGoat was used to create a controlled vulnerable AWS environment.

The scenario used was:

`iam_privesc_by_rollback`

CloudGoat used Terraform to provision the required AWS infrastructure.

Some of the setup and verification commands included:

```bash
cloudgoat config profile
aws configure list
aws configure list-profiles
aws sts get-caller-identity
cloudgoat --help
cloudgoat create iam_privesc_by_rollback
