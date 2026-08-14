# 🔐 Week 5– AWS IAM Architecture & Security Design

## Junior Cloud Security Engineer Internship | EncryptEdge Labs

### Task: AWS Identity and Access Management Architecture and Security Design

This week focused on securing AWS Identity and Access Management (IAM) by applying the **Principle of Least Privilege** in an isolated AWS lab environment.

The project involved creating and analyzing IAM users, groups, roles, and policies, identifying excessive permissions, redesigning access controls, validating permissions, and assessing IAM-related security risks.

---

## 🎯 Objectives

The main objectives of this project were to:

- Understand AWS IAM users, groups, roles, and policies
- Explore authentication and authorization in AWS
- Configure an isolated IAM security homelab
- Analyze IAM relationships and permissions
- Identify overly permissive IAM policies
- Apply the Principle of Least Privilege
- Validate IAM permissions using policy simulation
- Analyze IAM role trust relationships
- Map IAM security risks to MITRE ATT&CK
- Develop an IAM-focused cloud threat model
- Assess and prioritize IAM security risks

---

## 🛠️ Tools & Technologies

- Amazon Web Services (AWS)
- AWS Identity and Access Management (IAM)
- Amazon S3
- AWS CLI
- AWS CloudShell
- AWS Management Console
- AWS IAM Policy Simulator
- MITRE ATT&CK
- NIST SP 800-53
- CIS AWS Foundations Benchmark
- ISO 27001
- OWASP Cloud Security concepts

---

# 🏗️ Lab Architecture

The IAM homelab included:

### IAM User
`intern_user`

Used as the test identity for permission and access-control validation.

### IAM Group
`intern_group`

Used to manage permissions through group-based access control.

### IAM Role
`intern_role`

Used to explore role-based access control and AWS trust relationships.

### Amazon S3
`my-homelab-trail`

Used as the target resource for implementing and validating bucket-specific least-privilege permissions.

---

# Phase A – IAM Fundamentals & Policy Simulation

The first phase focused on understanding the core components of AWS IAM:

- Users
- Groups
- Roles
- Policies
- Authentication
- Authorization
- Trust relationships
- Least privilege

I used the **AWS IAM Policy Simulator** to test permissions and understand how AWS evaluates allowed and denied actions.

This phase demonstrated how overly broad permissions can increase the attack surface if an IAM identity is compromised.

---

# Phase B – AWS IAM Homelab Configuration

I created an isolated IAM environment within my AWS Free Tier account.

The following resources were configured:

- `intern_user`
- `intern_group`
- `intern_role`
- `AmazonS3ReadOnlyAccess`
- Custom `EC2DescribeInstances` inline policy

The IAM user was added to the group so permissions could be inherited through group-based access control.

### AWS CLI Verification

```bash
aws iam get-user --user-name intern_user

aws iam list-attached-group-policies \
  --group-name intern_group

aws iam list-group-policies \
  --group-name intern_group

aws iam get-role \
  --role-name intern_role
