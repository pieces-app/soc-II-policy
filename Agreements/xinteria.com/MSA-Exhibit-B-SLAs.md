# EXHIBIT B - SERVICE LEVEL AGREEMENTS

**Master Service Agreement - Attachment**  
**Effective Date:** [Same as MSA]

---

## 1. DEFINITIONS

**"Availability"** means the Service is accessible and operational for Customer use, excluding Scheduled Maintenance and Excused Downtime.

**"Business Hours"** means 9:00 AM - 5:00 PM ET, Monday through Friday, excluding public holidays. For specific engagements, SOW-defined hours control over this definition.

**"On-Call Hours"** means the hours outside of Business Hours during which Vendor maintains designated resources available for urgent support matters, subject to the scope and response times set forth in the applicable SOW or support policy.

**"Critical SLA Threshold"** means Service Availability falling below 95% in any calendar month.

**"Emergency Maintenance"** means urgent maintenance required to address security vulnerabilities or prevent service degradation.

**"Excused Downtime"** means unavailability that may result from:

- Scheduled Maintenance (with 72-hour notice and capped at 4 hours per month)
- The following, provided that Provider is using commercially reasonable efforts to mitigate any downtime:
  - Emergency Maintenance (with notice where possible)
  - Force Majeure events
  - Customer-caused issues
  - Third-party service failures beyond Provider's control
  - Subprocessor availability issues (including but not limited to LLM providers, authentication services (Descope), payment processors (Paddle))

**"Monthly Uptime Percentage"** = (Total Minutes in Month - Downtime Minutes) / Total Minutes in Month × 100

**"Scheduled Maintenance"** means planned maintenance performed during the Maintenance Window.

---

## 2. SERVICE AVAILABILITY COMMITMENTS

### 2.1 Availability Tiers

| Service Tier | Target Availability | Measurement Period | Critical Threshold |
|-------------|-------------------|-------------------|-------------------|
| **Standard** | 99.5% | Monthly | < 95% |
| **Premium** | 99.7% | Monthly | < 95% |
| **Enterprise** | 99.9% | Monthly | < 97% |

### 2.2 Availability Calculation
- Measured for cloud-hosted infrastructure and services only
- Includes persistent cloud storage and ephemeral processing services (including cloud proxy services for LLM operations)
- On-device software availability is Customer's responsibility
- Local SLM performance not included in SLA measurements
- Excludes Scheduled Maintenance (up to 4 hours/month)
- Excludes Excused Downtime

**Important Note on Subprocessor Dependencies:**
- Service availability for LLM features may be affected by third-party provider uptime (OpenAI, Anthropic, Google, etc.)
- BYOK configurations may be impacted by Customer's chosen LLM provider availability
- Authentication services (Descope) issues may affect SSO functionality
- Payment processing (Paddle) disruptions may impact billing and subscription management
- Provider SLA commitments apply only to Provider-controlled infrastructure

### 2.3 Service Credits

For each 0.1% below the uptime commitment, Customer receives a 5% service credit for the affected month, up to 100% maximum.

**Credit Request:** Customer must request credits within 90 days of the incident.

**Credit Application:** Credits apply to future invoices and do not result in refunds except as otherwise provided in the MSA.

---

## 3. SUPPORT RESPONSE TIMES

### 3.1 Severity Levels

**Severity 1 (Critical):**
- Definition: Complete service outage or data loss risk
- Initial Response: 
  - Standard: 4 hours
  - Premium: 1 hour
  - Enterprise: 30 minutes

**Severity 2 (High):**
- Definition: Major feature unavailable, significant performance degradation
- Initial Response:
  - Standard: 8 business hours
  - Premium: 4 hours
  - Enterprise: 2 hours

**Severity 3 (Medium):**
- Definition: Minor feature issue, workaround available
- Initial Response:
  - Standard: 24 business hours
  - Premium: 8 business hours
  - Enterprise: 4 business hours

**Severity 4 (Low):**
- Definition: General questions, feature requests
- Initial Response:
  - Standard: 48 business hours
  - Premium: 24 business hours
  - Enterprise: 8 business hours

### 3.2 Support Channels

| Tier | Email | Chat/Teams/Discord/Slack | Emergency Contact | Dedicated Channel |
|------|-------|--------------------------|-------------------|-----------------|
| Standard | ✓ | Business Hours | - | - |
| Premium | ✓ | Extended Hours | Cell phone for emergencies | - |
| Enterprise | ✓ | 24/7 | Cell phone for emergencies | ✓ |

---

## 4. MAINTENANCE WINDOWS

### 4.1 Scheduled Maintenance
- **Window:** Saturdays, 02:00 - 06:00 UTC
- **Frequency:** Maximum once per month
- **Notice:** 72-hour advance notice via email
- **Duration:** Maximum 4 hours per month

### 4.2 Emergency Maintenance
- **Notice:** Best effort advance notice
- **Communication:** Status page updates every 30 minutes
- **Duration:** Minimum necessary to resolve issue

---

## 5. PERFORMANCE METRICS

### 5.1 Response Time SLAs

| Metric | Target | Measurement |
|--------|--------|-------------|
| API Response Time (p95) | < 500ms | Monthly average |
| API Response Time (p99) | < 2000ms | Monthly average |
| AI Query Response | < 30 seconds | 95th percentile |

### 5.2 Data Processing SLAs

| Operation | Completion Target |
|-----------|------------------|
| Data Export Request | 48 hours |
| Data Deletion Request | 30 days |
| GDPR/CCPA Request | 30 days |
| Backup Recovery | 24 hours |

---

## 6. REPORTING AND MONITORING

### 6.1 Customer Access
- Real-time status page: status.pieces.app
- Monthly uptime reports
- Incident post-mortems for Severity 1 issues
- Quarterly business reviews (Enterprise only)

### 6.2 Measurement Tools
- Provider uses industry-standard monitoring tools
- Uptime measured via synthetic monitoring from multiple regions
- Customer may reasonably dispute measurements with supporting evidence

---

## 7. EXCLUSIONS AND LIMITATIONS

### 7.1 SLA Exclusions
- Beta features (service credits do not apply for beta features, but termination rights for material breach remain)
- Free tier services
- Customer-caused issues or misconfigurations, provided that Provider is using commercially reasonable mitigation efforts
- On-device software components
- Third-party integrations beyond Provider's control, provided that Provider is using commercially reasonable mitigation efforts
- Suspension for non-payment or AUP violations
- **Subprocessor Availability Issues that may include:**
  - LLM provider downtime or degradation (OpenAI, Anthropic, Google, etc.)
  - BYOK: Customer's chosen LLM provider availability issues
  - Authentication provider (Descope) outages or service disruptions
  - Payment processor (Paddle) disruptions affecting billing, licensing, or subscription management
  - Other subprocessor service degradation that may impact functionality
  - Provided in each case that Provider is using commercially reasonable mitigation efforts

### 7.2 Remedies
- **Service credits are Customer's sole remedy for isolated SLA failures that do not meet the critical SLA thresholds defined in Section 11 below.**
- **For persistent SLA failures meeting critical thresholds (as defined in Section 11), Customer has additional termination rights per MSA Section 1.4, which are separate from and in addition to service credits.**
- Credits do not entitle refunds or cash payment except as otherwise provided in the MSA
- Credits apply to individual month failures; termination rights apply to multi-month patterns

---

## 8. BYOK AND THIRD-PARTY DEPENDENCIES

### 8.1 BYOK Service Dependencies
When Customer uses Bring Your Own Key (BYOK) configurations:
- Service availability may be affected by Customer's chosen LLM provider uptime
- Provider is not responsible for LLM provider API availability or performance
- Customer is responsible for maintaining valid API keys and sufficient quota
- Provider's cloud proxy services need to be available for BYOK to function
- SLA credits do not apply for issues with Customer's LLM provider except as otherwise set forth herein

### 8.2 Subprocessor Service Dependencies
Provider's service availability may be affected by critical subprocessors:
- **Authentication (Descope):** May impact SSO and user access functionality
- **LLM Providers:** May affect AI feature availability (unless in Air-Gapped mode)
- **Cloud Infrastructure (GCP):** May impact all cloud services
- **Payment Processing (Paddle):** May affect billing operations, license validation, and subscription management
- **Note:** While Provider maintains redundancy and failover mechanisms where possible, subprocessor outages may still impact service availability

---

## 9. SLA MODIFICATIONS

### 9.1 Improvement Commitments
- Provider may improve SLAs at any time without notice
- Enterprise customers may lock SLAs for contract term

### 9.2 Measurement Adjustments
- Provider may adjust measurement methodology with 180 days notice
- Changes must not materially disadvantage Customer
- Historical data provided for comparison

---

## 10. CRITICAL SLA THRESHOLDS AND TERMINATION RIGHTS

**"Critical SLA Threshold"** for purposes of MSA Section 1.4:
- Service Availability below 95% (Standard/Premium tiers)
- Service Availability below 97% (Enterprise tier)
- Severity 1 response time exceeded by 4x target
- Data loss incident 
- Security Incident

**Measurement Period:** Rolling 12-month window

---

### ACCEPTANCE

This Exhibit B is incorporated by reference into the Master Service Agreement.

**Customer:** _______________________________  
**Date:** _______________

**Provider:** Mesh Intelligent Technologies, Inc.  
**Date:** _______________
