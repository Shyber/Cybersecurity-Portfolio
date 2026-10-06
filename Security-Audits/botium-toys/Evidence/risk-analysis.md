# Risk Analysis

## Overall Risk

**Risk Score: 8/10 — High**

The assessment identifies a relatively high level of risk due to
insufficient security controls and incomplete adherence to relevant
compliance practices.

## Major Risks

### 1. Unauthorized Access

**Risk:** High

Employees have broad access to internally stored information,
including potentially sensitive customer information.

**Potential Impact:**
- Unauthorized disclosure of PII/SPII
- Exposure of payment-card information
- Increased likelihood of insider-related incidents

**Recommended Mitigation:**
- Implement least privilege
- Implement role-based access control
- Review permissions regularly

---

### 2. Unencrypted Payment Information

**Risk:** High

Customer credit card information is stored, processed, and transmitted
internally without encryption.

**Potential Impact:**
- Exposure of payment information
- Financial loss
- Compliance issues
- Reputational damage

**Recommended Mitigation:**
- Encrypt sensitive data
- Protect data in transit and at rest
- Restrict access to payment information

---

### 3. Lack of Backups

**Risk:** High

Critical business data is not currently backed up.

**Potential Impact:**
- Data loss
- Business interruption
- Difficult or impossible recovery following an incident

**Recommended Mitigation:**
- Implement regular backups
- Test restoration procedures
- Protect backup copies from unauthorized access

---

### 4. Lack of Disaster Recovery Planning

**Risk:** High

No disaster recovery plan is currently in place.

**Potential Impact:**
- Extended service disruption
- Loss of business operations
- Increased recovery time

**Recommended Mitigation:**
- Develop a disaster recovery plan
- Define recovery priorities
- Test the plan regularly

---

### 5. Lack of Intrusion Detection

**Risk:** Medium–High

The organization has a firewall but no intrusion detection system.

**Potential Impact:**
- Malicious activity may not be detected quickly
- Increased incident response time

**Recommended Mitigation:**
- Implement IDS/monitoring capabilities
- Establish alert investigation procedures