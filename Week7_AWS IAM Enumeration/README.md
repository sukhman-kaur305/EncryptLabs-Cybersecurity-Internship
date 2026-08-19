# AWS IAM Enumeration & Privilege Escalation Risk Analysis

## Overview

This project focuses on AWS Identity and Access Management (IAM) enumeration, permission analysis, and identification of security risks caused by excessive or misconfigured access.

A controlled AWS lab environment using CloudGoat was used to enumerate IAM identities, analyze permissions and trust relationships, identify potential privilege-escalation paths, assess risks, and recommend security controls based on least-privilege principles.

> **Authorization:** All testing was performed only within authorized AWS and hosted training environments. No production systems or customer data were accessed.

---

## Project Objectives

- Understand AWS IAM enumeration techniques.
- Enumerate IAM users, groups, roles, and policies.
- Analyze IAM permissions and role trust relationships.
- Identify potential privilege-escalation paths.
- Review external and cross-account exposure using IAM Access Analyzer.
- Translate technical IAM findings into business risk.
- Recommend technical and governance controls.

---

## Lab Environment

| Component | Purpose |
|---|---|
| AWS IAM | Identity, role, and policy enumeration |
| CloudGoat | Vulnerable AWS IAM lab environment |
| Terraform | CloudGoat infrastructure deployment |
| AWS CLI | IAM enumeration and configuration analysis |
| IAM Access Analyzer | External and cross-account access analysis |
| Policy Sentry | IAM policy analysis/testing |
| Steampipe | SQL-based cloud enumeration testing |
| PwnedLabs | AWS credential abuse training |
| Cybr | IAM credential report training |

**AWS Region:** `us-east-2`

**CloudGoat Scenario:**

`iam_privesc_by_attachment`

---

## Project Phases

### Phase A – Theory & Introduction

Reviewed AWS IAM fundamentals, including:

- IAM users and roles
- Managed and inline policies
- Role trust relationships
- Explicit and implicit permissions
- IAM enumeration techniques
- Privilege-escalation concepts

Example enumeration commands:

```bash
aws iam list-users
aws iam list-policies
aws iam list-roles
aws iam get-role --role-name <ROLE_NAME>
