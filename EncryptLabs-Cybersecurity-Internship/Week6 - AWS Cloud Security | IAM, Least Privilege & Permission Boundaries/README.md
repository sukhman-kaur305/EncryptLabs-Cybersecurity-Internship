# 🔐 AWS IAM Least Privilege & Permission Boundaries Lab

## Junior Cloud Security Engineer Internship — Week 6

This project focuses on securing AWS Identity and Access Management (IAM) through **least-privilege policy engineering, IAM policy simulation, permissions boundaries, privilege-escalation analysis, and cloud risk assessment**.

The lab demonstrates how excessive IAM permissions can increase an organization's cloud attack surface and how preventive controls can reduce the impact of compromised credentials.

---

## 🎯 Objectives

The main objectives of this project were to:

- Understand AWS IAM and the principle of least privilege
- Design IAM policies based on business requirements
- Validate policies using the AWS IAM Policy Simulator
- Explore IAM privilege-escalation paths
- Implement AWS permissions boundaries
- Analyze how permissions boundaries reduce credential blast radius
- Map cloud threats to MITRE ATT&CK
- Assess identified risks using a risk matrix
- Develop remediation and security recommendations

---

## 🛠️ Technologies & Tools

- AWS IAM
- AWS CLI
- AWS IAM Policy Simulator
- Terraform
- BishopFox IAM Vulnerable
- Kali Linux
- Visual Studio Code
- Git / GitHub
- MITRE ATT&CK

---

## 🧪 Lab Environment

All activities were performed within an **authorized, non-production AWS sandbox environment**.

The local environment consisted of Kali Linux configured with AWS CLI, Terraform, Git, and VS Code.

The **IAM Vulnerable** project was used as an intentionally vulnerable IAM training environment for examining privilege-escalation paths.

> No production systems, third-party AWS accounts, or real customer data were accessed during this project.

---

# Phase A — IAM & Least Privilege

The first phase focused on understanding AWS IAM authorization and the principle of least privilege.

A custom S3 read-only policy was reviewed and created to demonstrate how permissions can be restricted to required actions.

Example:

```json
{
  "Effect": "Allow",
  "Action": [
    "s3:ListBucket",
    "s3:GetObject"
  ],
  "Resource": [
    "arn:aws:s3:::example-bucket",
    "arn:aws:s3:::example-bucket/*"
  ]
}
