# Secure Coding Checklist - Medpay Vault

## 1. Input Validation & Sanitization
- [ ] Validate all user inputs on both client and server sides.
- [ ] Prevent SQL Injection by using parameterized queries / ORM for Amazon RDS.
- [ ] Sanitize outputs to prevent Cross-Site Scripting (XSS).

## 2. Authentication & Session Management
- [ ] Enforce strong password policies and Multi-Factor Authentication (MFA) where applicable.
- [ ] Secure session tokens and ensure tokens expire appropriately.

## 3. Secrets & Configuration Management
- [ ] Never hardcode API keys, database passwords, or secrets in the source code.
- [ ] Use environment variables and **AWS Secrets Manager** / Parameter Store.
- [ ] Enable **GitHub Secret Scanning** and Dependabot alerts to catch exposed credentials and vulnerable dependencies.

## 4. Encryption & Data Protection
- [ ] Use HTTPS/TLS for all data in transit.
- [ ] Enable encryption at rest for databases (RDS) and object storage (S3) using AWS KMS.
