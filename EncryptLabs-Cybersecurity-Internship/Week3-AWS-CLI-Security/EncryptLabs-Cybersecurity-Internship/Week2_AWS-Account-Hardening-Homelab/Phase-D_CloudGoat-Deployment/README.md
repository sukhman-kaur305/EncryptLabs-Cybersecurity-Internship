# Phase D – CloudGoat & iam-vulnerable Deployment

**Objective:** Deploy CloudGoat and iam-vulnerable safely within isolated subnets.
**Estimated Time:** ~180 minutes

## What I Did
- Cloned CloudGoat and iam-vulnerable repos onto an EC2 management instance
- Deployed CloudGoat's `ec2_ssrf` scenario using its default configuration
- Deployed iam-vulnerable using Terraform (`terraform init` / `terraform apply`)
- Verified EC2 instances, security groups, subnets, and Network ACLs via AWS CLI

## Files
- `Deploy_CloudGoat.png` – CloudGoat deployment command output
- `terraform_apply.png` – Terraform deployment success
- `ec2_ssrf.png` – CloudGoat SSRF scenario confirmation
- `EC2_Instance.png` – CLI output of EC2 instance details
- `Lab_Instances.png` – Console view of deployed lab instances
- `Network_ACL.png` / `Network_ACL_IP.png` – Network ACL configuration
- `Solu_User_Login.png` – Lab-generated credentials verification

## Key Takeaway
[1-2 sentences on your main insight]
