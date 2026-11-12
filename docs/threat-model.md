# Threat Modeling & STRIDE Analysis - Medpay Vault

## 1. Project Overview
Medpay Vault is a secure cloud application designed to process medical payments and handle sensitive health-related financial transactions securely on AWS.

## 2. STRIDE Threat Matrix

| Threat Category | Potential Threat Description | Security Control / Mitigation |
| :--- | :--- | :--- |
| **Spoofing** | Attacker impersonating a patient or medical staff. | Enforce AWS Cognito / IAM authentication, TLS encryption in transit. |
| **Tampering** | Unauthorized modification of payment transactions or medical records. | Use AWS KMS for data encryption at rest, integrity checks via CodeQL and Git. |
| **Repudiation** | Users denying actions performed on the payment gateway. | Enable AWS CloudTrail and CloudWatch logging for audit trails. |
| **Information Disclosure** | Leakage of sensitive patient data or database credentials. | Encrypt S3 buckets, use AWS Secrets Manager, enable GitHub Secret Scanning. |
| **Denial of Service (DoS)** | Overwhelming the application or API endpoints to disrupt service. | Deploy AWS WAF, Auto Scaling groups, and Application Load Balancer. |
| **Elevation of Privilege** | Normal user gaining administrative access to AWS resources. | Implement AWS IAM Least Privilege principle and Role-Based Access Control (RBAC). |
