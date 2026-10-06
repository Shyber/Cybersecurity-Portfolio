# Botium Toys — Internal Security Audit

## Overview

This project documents an internal security audit conducted for **Botium Toys**, a fictional small U.S.-based toy company with both physical and online operations.

The objective of the audit was to evaluate the organization's current security posture, identify gaps in security controls and compliance practices, and provide recommendations to reduce risks to business assets and sensitive information.

This project was completed as part of the **Google Cybersecurity Professional Certificate**.

> **Disclaimer:** Botium Toys is a fictional organization used for cybersecurity training. This repository is an independent portfolio project and is not affiliated with or endorsed by Google.

---

## Scenario

Botium Toys operates from a single physical location that serves as its main office, retail storefront, and warehouse. The company has also expanded its online presence and now serves customers in the United States and internationally.

As the organization grows, its IT department faces increasing pressure to maintain business operations while protecting company and customer information.

The IT manager initiated an internal security audit to:

* Assess the organization's existing security controls
* Identify security risks and vulnerabilities
* Evaluate compliance-related practices
* Protect critical business and customer data
* Improve the organization's overall security posture

The audit covers the organization's security program, including employee devices, internal systems, networks, and other IT-managed assets.

---

## Audit Scope

The audit covers the organization's overall security program and the assets managed by the IT department.

### Assets considered

* On-premises IT equipment
* Employee desktops, laptops, smartphones, and remote workstations
* Network equipment and internal network infrastructure
* Business applications and services
* Accounting and database systems
* E-commerce and inventory management systems
* Security systems and surveillance equipment
* Internet access
* Data storage and retention
* Legacy systems requiring manual monitoring
* Physical products stored in the warehouse

The audit scope and asset inventory are based on the organization's internal scope and risk assessment report.

---

## Audit Objectives

The primary objectives were to:

1. Review the organization's existing security controls.
2. Identify missing or insufficient controls.
3. Assess risks to critical assets.
4. Evaluate selected PCI DSS, GDPR, and SOC-related practices.
5. Identify areas requiring improvement.
6. Provide security recommendations to reduce organizational risk.

The organization's reported risk score was **8/10**, indicating a relatively high level of risk caused by gaps in security controls and compliance practices.

---

# Security Controls Assessment

The controls assessment evaluates whether specific security controls are currently implemented at Botium Toys.

| Security Control                 | Status               | Assessment                                                                                              |
| -------------------------------- | -------------------- | ------------------------------------------------------------------------------------------------------- |
| Least Privilege                  | ❌ No                 | Employees currently have broad access to internally stored data.                                        |
| Disaster Recovery Plans          | ❌ No                 | No disaster recovery plan is currently documented.                                                      |
| Password Policies                | ✅ Yes                | A password policy exists, although its requirements are insufficient.                                   |
| Separation of Duties             | ❌ No                 | Separation of duties has not been implemented.                                                          |
| Firewall                         | ✅ Yes                | A firewall is implemented and uses defined security rules.                                              |
| Intrusion Detection System (IDS) | ❌ No                 | No IDS has been installed.                                                                              |
| Backups                          | ❌ No                 | Critical data is not currently backed up.                                                               |
| Antivirus Software               | ✅ Yes                | Antivirus software is installed and regularly monitored.                                                |
| Legacy System Monitoring         | ⚠️ Needs Improvement | Legacy systems are monitored, but there is no regular schedule and intervention procedures are unclear. |
| Encryption                       | ❌ No                 | Customer payment information is not encrypted.                                                          |
| Password Management System       | ❌ No                 | No centralized password management system is implemented.                                               |
| Physical Locks                   | ✅ Yes                | Offices, storefront, and warehouse have appropriate locks.                                              |
| CCTV Surveillance                | ✅ Yes                | Up-to-date CCTV surveillance is in place.                                                               |
| Fire Detection/Prevention        | ✅ Yes                | Fire detection and prevention systems are functioning.                                                  |

## The assessment is based on the controls and findings documented in the Botium Toys risk assessment.

# Compliance Assessment

## PCI DSS

Payment Card Industry Data Security Standard (PCI DSS) practices were reviewed because Botium Toys accepts, processes, transmits, and stores customer payment information.

| PCI DSS Area                              | Status | Finding                                                                                                                          |
| ----------------------------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------- |
| Restrict access to cardholder information | ❌ No   | Employees have broad access to internally stored data and may access cardholder information.                                     |
| Secure payment-data environment           | ❌ No   | Payment information is stored and processed internally without sufficient encryption.                                            |
| Encryption                                | ❌ No   | Encryption is not currently used to protect customer credit card information.                                                    |
| Secure password management                | ❌ No   | Existing password controls do not meet appropriate security requirements and there is no centralized password management system. |

The risk assessment specifically identifies unrestricted access to cardholder information, lack of encryption, and insufficient access controls as security concerns.

---

# GDPR Assessment

Because Botium Toys serves customers in the European Union, GDPR-related practices were also evaluated.

| GDPR Area                         | Status | Finding                                                                                          |
| --------------------------------- | ------ | ------------------------------------------------------------------------------------------------ |
| Protect EU customer data          | ❌ No   | Existing access controls do not sufficiently restrict access to sensitive customer information.  |
| 72-hour breach notification       | ✅ Yes  | A plan exists to notify EU customers within 72 hours of a security breach.                       |
| Data classification and inventory | ❌ No   | The organization has inadequate asset management and has not sufficiently classified its assets. |
| Privacy policies and procedures   | ✅ Yes  | Privacy policies, procedures, and processes have been developed and are enforced.                |

## The risk assessment confirms that a 72-hour notification plan and privacy procedures are in place, while asset management and classification remain areas requiring improvement.

# SOC Assessment

The assessment also considers practices related to **System and Organization Controls (SOC)**.

| SOC Practice                   | Status | Assessment                                                                      |
| ------------------------------ | ------ | ------------------------------------------------------------------------------- |
| User access policies           | ❌ No   | Appropriate access restrictions have not been fully implemented.                |
| Sensitive data confidentiality | ❌ No   | Broad employee access creates a confidentiality risk for PII/SPII.              |
| Data integrity                 | ✅ Yes  | The IT department has implemented controls intended to maintain data integrity. |
| Data availability              | ✅ Yes  | Availability controls have been implemented.                                    |

The assessment identifies data integrity and availability as areas where controls are already present, while access control and sensitive-data confidentiality require improvement.

---

# Key Findings

The audit identified several significant security gaps.

### 1. Excessive access to sensitive information

Employees currently have broad access to internally stored information. This may expose customer personally identifiable information (PII/SPII) and payment-card data to unauthorized users.

**Risk:** Unauthorized disclosure or misuse of sensitive information.

**Recommended action:** Implement role-based access control and the principle of least privilege.

---

### 2. Lack of encryption

Customer credit card information is stored, processed, and transmitted internally without encryption.

**Risk:** Sensitive payment information could be exposed if systems or communications are compromised.

**Recommended action:** Implement encryption for sensitive data both at rest and in transit.

---

### 3. No disaster recovery plan

The organization does not currently have a documented disaster recovery plan.

**Risk:** A major incident could significantly disrupt business operations.

**Recommended action:** Develop and regularly test a disaster recovery and business continuity plan.

---

### 4. No critical-data backups

Critical business data is not currently backed up.

**Risk:** Data could be permanently lost following hardware failure, cyberattack, or another disruptive event.

**Recommended action:** Implement regular, tested backups and maintain appropriate backup copies.

---

### 5. No intrusion detection system

The IT department has implemented a firewall but does not currently use an IDS.

**Risk:** Malicious or suspicious network activity may not be detected quickly.

**Recommended action:** Deploy an intrusion detection and monitoring capability and establish an incident-response process.

---

### 6. Weak password controls

A password policy exists, but its requirements are considered insufficient. There is also no centralized password management system.

**Risk:** Weak or reused passwords may increase the likelihood of unauthorized access.

**Recommended action:** Strengthen password requirements and implement centralized password management.

---

### 7. Legacy system management requires improvement

Legacy systems are monitored and maintained, but there is no consistent schedule and intervention procedures are unclear.

**Risk:** Vulnerabilities or failures in legacy systems may remain undetected.

**Recommended action:** Establish documented monitoring, maintenance, and intervention procedures.

---

# Recommendations

Based on the audit findings, the following improvements should be prioritized:

1. **Implement least-privilege access controls**

   * Restrict access according to job responsibilities.
   * Review user permissions regularly.

2. **Implement separation of duties**

   * Ensure critical activities are not controlled by a single individual.

3. **Encrypt sensitive information**

   * Protect payment-card data and other sensitive customer information.

4. **Implement reliable backups**

   * Back up critical systems and data regularly.
   * Test restoration procedures.

5. **Develop a disaster recovery plan**

   * Define recovery procedures, responsibilities, and priorities.
   * Test the plan periodically.

6. **Deploy intrusion detection**

   * Monitor network activity for suspicious behavior.
   * Establish procedures for investigating alerts.

7. **Improve password security**

   * Strengthen password requirements.
   * Use centralized password management.

8. **Improve asset management**

   * Maintain an accurate inventory of hardware, software, systems, and data.
   * Classify assets according to their importance and sensitivity.

9. **Improve legacy-system management**

   * Establish regular monitoring and maintenance schedules.
   * Document intervention procedures.

10. **Perform regular security reviews**

    * Reassess controls and compliance requirements as the organization grows.

---

# Risk Summary

The organization's current risk score is **8/10**, which indicates a relatively high level of risk.

The most significant areas of concern are:

* Excessive access to sensitive information
* Lack of encryption
* Lack of backups
* Lack of disaster recovery planning
* Missing intrusion detection
* Weak password management
* Insufficient asset classification and management

Addressing these gaps would improve Botium Toys' ability to protect sensitive information, maintain business continuity, and meet applicable security and compliance expectations.

---

# Skills Demonstrated

This project demonstrates practical knowledge of:

* Internal security auditing
* Security controls assessment
* Risk assessment
* NIST Cybersecurity Framework concepts
* Access control
* Least privilege
* Network security
* Data protection
* Encryption
* Backup and disaster recovery
* Password security
* Physical security
* PCI DSS
* GDPR
* SOC concepts
* Security recommendations
* Cybersecurity documentation

---

# Frameworks & Standards Reviewed

* **NIST Cybersecurity Framework (NIST CSF)**
* **Payment Card Industry Data Security Standard (PCI DSS)**
* **General Data Protection Regulation (GDPR)**
* **System and Organization Controls (SOC)**

---

## Conclusion

The internal audit shows that Botium Toys has several foundational security controls in place, including a firewall, antivirus protection, physical security, CCTV, fire detection, and controls supporting data integrity and availability.

However, significant gaps remain in access control, encryption, backups, disaster recovery, intrusion detection, password management, and asset management.

Prioritizing these areas would substantially improve the organization's security posture and reduce the potential impact of security incidents and compliance-related risks.
