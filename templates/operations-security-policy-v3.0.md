**Vanta policy template instructions**

This Vanta policy template represents a complete, compliance-ready policy with placeholders for company specific text. Each policy section represents a policy-specific topic that you should consider and/or modify to match your company’s practices.

**For each policy section**

* Consider if this section and its corresponding risks apply to you. If it does not, remove it and/or replace it with your organization’s corresponding practices.  
* Replace any highlighted text in angled brackets \< \>[^1] with your own language  
* Rewrite the policy language such that it reflects the practices of your organization

**Policy completion checklist**

1. Use Find to make sure that all text in angled brackets is replaced  
2. Proofread your policy for spelling and grammar mistakes  
3. Confirm that the policy’s content reflects your organizations practices  
4. Add any company-specific letterhead, branding, and formatting  
5. Remove this instructions page  
6. Export this document as PDF — File \> Save As \> Change “File Format” to PDF  
7. Upload the PDF to Vanta at [https://app.vanta.com/policies](https://app.vanta.com/policies)

**More questions?**

A good rule-of-thumb is to keep your language at a high enough level such that it stays representative for at least a year. If you have more questions about how to use this template, please reach out to [support@vanta.com](mailto:support@vanta.com) or your auditor for additional guidance.

# **Operations Security Policy** 

**Policy Owner:** \<Policy owner\>

**Effective Date:** \<Effective date\> 

# **Purpose** 

To ensure the correct and secure operation of information processing systems and facilities.

# **Scope** 

All \<Company Name\> information systems that are business critical and/or process, store, or transmit company data. This Policy applies to all employees of \<Company Name\> and other third-party entities with access to \<Company Name\> networks and system resources.

# **Operations Security**

## **Documented Operating Procedures**

Both technical and administrative operating procedures shall be documented as needed and made available to all users who need them.

## **Change Management**

Changes to the organization, business processes, information processing facilities, production software and infrastructure, and systems that affect information security in the production environment and financial systems shall be tested, reviewed, and approved prior to production deployment. All significant changes to in-scope systems and networks must be documented.

1\. Change Documentation and Review:

* All significant changes to systems, networks, and processing facilities must be documented.  
* The documentation must encompass the change's purpose, specification, potential impact considering dependencies, and deployment plan.  
* Changes should be tested and reviewed in environments segregated from both production and development (e.g., staging environments).

2\. Approval and Authorization:

* Changes with substantial impact on information security and operational functionalities, must obtain formal authorization before deployment.  
* Emergency changes may be expedited but must undergo a retrospective review and authorization.

3\. Change Management Procedures:

* Planning and Impact Assessment: Evaluate potential impacts of the changes considering system dependencies.  
* Authorization: Secure necessary approvals before initiating changes  
* Communication: Inform relevant internal and external stakeholders about the planned changes, schedules, and expected impact in advance.  
* Testing and Quality Control: Ensure changes are tested thoroughly (refer to section 8.29 for testing and acceptance specifics) and meet quality standards before implementation.  
* Implementation and Deployment: Execute changes in alignment with the planned deployment schedule  
* Emergency Management: Remediation: If changes fail or present unexpected issues, they shall be reverted  
* Documentation Maintenance: Ensure that the ticketing systems or the code repository platform keeps record of changes, commits and deployments.

4\. Continuity and Consistency:

* Ensure that the ICT continuity plans, response, and recovery procedures are updated to remain appropriate and consistent with the changes made.  
* Ensure operating documentation and user procedures are modified and remain suitable.

5\. Security and Integrity:

* Ensure that changes preserve and do not compromise the confidentiality, integrity, and availability of information in processing facilities and systems.

## **Capacity Management**

The use of processing resources and system storage shall be monitored and adjusted to ensure that system availability and performance meets \<Company Name\> requirements.

Human resource skills, availability, and capacity shall be reviewed and considered as a component of capacity planning and as part of the annual risk assessment process.

Scaling resources for additional processing or storage capacity, without changes to the system, can be done outside of the standard change management and code deployment process.

## **Data Leakage Prevention**

In adherence to this Data Leakage Prevention Policy, and in order to minimize the risk of leakage of sensitive information, the organization shall:

* Identify and classify information in accordance with the Data Management Policy  
* Provide awareness training to users including the appropriate use and handling of sensitive information

Consider the use of technical monitoring and Data Loss Prevention (DLP) tools in accordance with the risks to the organization and data subjects

## **Web Filtering**

The organization shall ensure safe, secure, and appropriate internet use by the organization’s personnel.

Website Access and Blocking:

* Implement mechanisms, such as secure DNS and IP address or domain blocking, to restrict access to websites that pose a substantial risk due to their content or known distribution of malware, viruses, or phishing materials.  
* Employ browsers and anti-malware technologies capable of automatic website blocking or configuration for the same.  
* Unless justified by legitimate business reasons, consider blocking access to websites with:  
1. Information upload capabilities.  
2. Known or suspected malicious content.  
3. Act as command and control servers.  
4. Identified as malicious through threat intelligence.  
5. Sharing of illegal content.

Usage Rules and Guidelines:

* User shall conform to all company rules in accordance with the Code of Conduct and the Acceptable Use Policy found in the Information Security Policy.

## **Separation of Development, Staging and Production Environments[^2]**

Development and staging environments shall be strictly segregated from production SaaS environments to reduce the risks of unauthorized access or changes to the operational environment. Confidential production customer data must not be used in development or test environments without the express approval of the \<approver of the use of customer data, e.g., VP of Customer Support\>. 

Refer to the Data Management Policy[^3] for a description of Confidential data. If production customer data is approved for use in the course of development or testing, it shall be scrubbed of any such sensitive information whenever feasible.

# **Systems and Network Configuration, Hardening, and Review**

Systems and networks shall be provisioned and maintained in accordance with the configuration and hardening standards described in Appendix A[^4] to this policy.

Firewalls and/or appropriate network access controls and configurations shall be used to control network traffic to and from the production environment in accordance with this policy. 

Production network access configuration rules shall be reviewed at least annually. Tickets shall be created to obtain approvals for any needed changes.

# **Protection from Malware**

In order to protect the company’s infrastructure against the introduction of malicious software, detection, prevention, and recovery controls to protect against malware shall be implemented, combined with appropriate user awareness.

Anti-malware protections shall be utilized on all company-issued endpoints except for those running operating systems not normally prone to malicious software. Additionally, threat detection and response software shall be utilized for company email. The anti-malware protections utilized shall be capable of detecting common forms of malicious threats and performing the appropriate mitigation activity (such as removing, blocking or quarantining).

\<Company Name\> should scan all files upon their introduction to systems, and continually scan files upon access, modification, or download. Anti-malware definition and engine updates should be configured to be downloaded and installed automatically whenever new updates are available.  Known or suspected malware incidents must be reported as a security incident. 

It is a violation of company policy to disable or alter the configuration of anti-malware protections without authorization.

# **Information Backup**

The need for backups of systems, databases, information and data shall be considered and appropriate backup processes shall be designed, planned and implemented. Backup procedures must include procedures for maintaining and recovering customer data in accordance with documented SLAs[^5]. Security measures to protect backups shall be designed and applied in accordance with the confidentiality or sensitivity of the data. Backup copies of information, software and system images shall be taken regularly to protect against loss of data. Backups and restore capabilities shall be periodically tested, not less than annually.

Backups must be stored separately (\<describe specific requirements for separate region or availability zone\>) from the production data location[^6]. 

\<Company Name\> does not regularly backup user devices like laptops. Users are expected to store critical files and information in company-sanctioned file storage repositories.  

Backups are configured to run \<frequency of backups, e.g., daily\> on in-scope systems. The backup schedules are maintained within the backup application software. 

A backup restore test should be performed at least annually to validate the backup data and backup process[^7].

# **Logging & Monitoring**

Production infrastructure shall be configured to produce detailed logs appropriate to the function served by the system or device. Event logs recording user activities, exceptions, faults and information security events shall be produced, kept and reviewed through manual or automated processes as needed. Appropriate alerts shall be configured for events that represent a significant threat to the confidentiality, availability or integrity of production systems or Confidential data.

Logging should meet the following criteria for production applications and supporting infrastructure[^8]:

* Log user log-in and log-out  
* Log CRUD (create, read, update, delete) operations on application and system users and objects  
* Log security settings changes (including disabling or modifying of logging)  
* Log application owner or administrator access to customer data (i.e. Access Transparency)  
* Logs must include user ID, IP address, valid timestamp, type of action performed, and object of this action.   
* Logs must be stored for at least 30 days, and should not contain sensitive data or payloads

## **Protection of Log Information**

Logging facilities and log information shall be protected against tampering and unauthorized access.

## **Administrator & Operator Logs**

System administrator and system operator activities shall be logged and reviewed and/or alerted in accordance with the system classification and criticality.

## **Data Restore Logs[^9]**

In the event the company needs to restore production data containing PII from backups, either for the purposes of providing services or for testing purposes, shall be logged or tracked in auditable tickets.

## **Clock Synchronization**

The clocks of all relevant information processing systems within an organization or security domain shall be synchronized to network time servers using reputable time sources.

## **File Integrity Monitoring and Intrusion Detection[^10]**

\<Company Name\> production systems shall be configured to monitor, log, and self-repair and/or alert on suspicious changes to critical system files where feasible.

Alerts shall be configured for suspicious conditions and engineers shall review logs on a regular basis.

Unauthorized intrusions and access attempts or changes to \<Company Name\> systems shall be investigated and remediated in accordance with the Incident Response Plan.

# **Control of Operational Software**

The installation of software on production systems shall follow the change management requirements defined in this policy.

# **Threat Intelligence**

Information relating to information security threats should be collected and analyzed to produce threat intelligence.

Collection: Draw from diverse sources, such as blogs, news articles, vendor updates, public databases, and industry communities.

Analysis: Examine the data to derive actionable insights and enable proactive response initiatives. Report any actionable insights or specific threats to the Security Team.

Dissemination: Ensure effective communication of threat intelligence to pertinent teams for effective action. The Security Team shall disseminate actionable information via communication channels, such as slack, email and emergency alerts.

Feedback: Cultivate continuous improvement by leveraging feedback for policy enhancements. Integrate feedback into policy amendments and conduct regular policy reviews.

# **Technical Vulnerability Management[^11]**

Information about technical vulnerabilities of information systems being used shall be obtained in a timely fashion, the organization's exposure to such vulnerabilities shall be evaluated, and appropriate measures taken to address the associated risk. A variety of methods shall be used to obtain information about technical vulnerabilities, including \<vulnerability scanning, penetration tests, review of external vendor alerts, and the bug bounty program\>.

Vulnerability scans shall be performed on public-facing systems in the production environment at least \<quarterly\>. 

Penetration tests of the applications and production network shall be performed at least annually, and additional scanning and testing shall be performed following major changes to production systems and software.

The \<IT and Engineering\> departments shall evaluate the severity of vulnerabilities identified from any source, and if it is determined to be a risk-relevant critical or high-risk vulnerability, a service ticket will be created. The \<Company Name\> assessed severity level may differ from the level automatically generated by scanning software or determined by external researchers based on \<Company Name\>’s internal knowledge and understanding of technical architecture and real-world impact/exploitability. Tickets are assigned to the system, application, or platform owners for further investigation and/or remediation.

Vulnerabilities assessed by \<Company Name\> shall be patched or remediated in the following timeframes[^12]:

| Determined Severity | Remediation Time |
| ----- | ----- |
| Critical | 30 Days |
| High | 30 Days |
| Medium | 60 Day |
| Low | 90 Days |
| Informational | As needed |

Service tickets for any vulnerability which cannot be remediated within the standard timeline must show a risk treatment plan and planned remediation timeline.

# **Restrictions on Software Installation**

Rules governing the installation of software by users shall be established and implemented in accordance with the \<Company Name\> Information Security Policy[^13].

# **Information Systems Audit Considerations**

Audit requirements and activities involving verification of operational systems shall be carefully planned and agreed to minimize disruptions to business processes.

# **Systems Security Assessment & Requirements** 

Risks shall be considered prior to the acquisition of, or significant changes to, systems, technologies, or facilities. Where requirements are formally identified, any relevant security requirements shall be included. The acquisition of new suppliers and services shall be made in accordance with the Third-Party Management Policy[^14].

The company shall perform an annual network security assessment that includes a review of major changes to the environment such as new system components and network topology.

# **Data Masking**

\[Optional\] \<Company Name\> will implement data masking based on risk or a specific requirement to do so.

Techniques Guidance:

* Adopt appropriate techniques such as data masking, pseudonymization, or anonymization to protect PII and other sensitive data effectively.  
* Guarantee that pseudonymization and anonymization methods effectively break the link between PII and individuals or sensitive data elements.  
* Confirm all elements of the information are considered for adequate data anonymization.  
* Employ additional data masking methods, such as encryption, character nulling/deleting, varying numbers and dates, substitution, and replacing values with their hashes.

Data Masking Considerations:

* Design data queries and masks to disclose only the minimally required data to users, safeguarding privacy and security.  
* Develop mechanisms for data obfuscation, considering specific circumstances under which certain data should be concealed from users.  
* Provide options for PII principals to control the visibility of their obfuscated data and adhere to any applicable legal or regulatory requirements related to data masking.

Using Data Masking, Pseudonymization, or Anonymization:

* Determine the suitable strength level, access controls, user agreements, and usage restrictions for processed data.  
* Prevent the combination of processed data with other information to identify PII principals and ensure traceability of provided and received processed data.

# **Exceptions**

Requests for an exception to this policy must be submitted to the \<approver of exceptions to this policy, e.g., IT Manager\> for approval.

# **Violations & Enforcement**

Any known violations of this policy should be reported to the \<person who should receive reports of violations of this policy, e.g., IT Manager\>. Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :---: | :---: | :---: |
| \<1.0\> | \<29-Apr-2020\> | \<First Version\> | \<OWNER\> | \<APPROVER\> |
|  |  |  |  |  |

# **APPENDIX A \- Configuration and Hardening Standards**

\<NOTE TO CUSTOMER: Templates are provided as informational reference. Standards like SOC2 and ISO 27001 do not prescribe any particular configuration or hardening. Further guidance can be found in ISO 27002 for Control A.8.9 Configuration Management \- Remove this language from the policy upon edit\>

\<Configuration and hardening standards shall be maintained on the internal documentation portal.\>

\<link\>[^15]

\<Include links to external sources, or internally created samples:\>

\<[https://aws.amazon.com/compliance/resources/](https://aws.amazon.com/compliance/resources/)\>

\<Address baseline config management and deployment per control 3.4, 7.1\>

**\<Servers and Virtual Machines\>[^16]**

\<This is the standard for system-level server and virtual server (VM) configuration hardening. Some customization to these settings may be required  to configure the system for its specific target environment, such as setting the proper names, groups, authentication settings, and other personalization options.\>

\<INSERT OS/SYSTEM BASELINE\>[^17]

\<In addition to the requirements to secure systems to the baseline outlined above, all physical and virtual systems must adhere to the following technical requirements:\>

* \<All vendor default passwords (including default passwords on operating systems, software providing security services, application and system accounts, Simple Network Management Protocol (SNMP) community strings, etc.) must be changed before a system is installed on the network.\>  
* \<Unnecessary default accounts (including accounts used by operating systems, security software, applications, systems, SNMP, etc.) must be removed or disabled before a system is installed on the network.\>  
* \<Only one primary function may be implemented per server or virtual machine to prevent functions that require different security levels from coexisting on the same system.\>  
* \<Only necessary services, protocols, daemons, etc., may be enabled, and only as required for the function of the system.  All unnecessary functionality (such as scripts, drivers, features, subsystems, file systems, and unnecessary web servers) must be disabled.\>  
* \<All security patches identified as \<critical, high, or medium\> must be applied to systems within SLAs established in this policy.\>

**\<Network Standards\>**

* \<Management of network rules and settings may only be performed by authorized members of \<ENGINEERING TEAM etc.\> and all changes must comply with change Management procedures defined in the Operations Security Policy.\>

* \<Supported network controls for production networks are \<TYPE e.g. AWS NACLs\>. Management of production network systems is accomplished through the use of \<MANAGEMENT SYSTEM, SSH, ETC\>\>  
    
* \<In the \<PRODUCTION ENVIRONMENT\>, defined rules and configurations must be enforced to control traffic from untrusted networks (e.g. publicly available services) to internal production networks\>  
    
* \<Network control systems must be configured to use default Network Address Translation to prevent the disclosure of internal IP addresses to the Internet.\>  
    
* \<Mobile devices connecting to production networks must meet the requirements of the Mobile Device Policy found in the Information Security Policy.\>  
    
* \<All network control systems must be configured with default antispoofing rules to block or deny inbound internal addresses originating from the Internet\>  
* \<External configurations must limit inbound traffic to only system components that provide authorized publicly accessible services, protocols, and ports.\>

* \<Use of insecure services and protocols without justification and documentation of additional security features implemented to mitigate risk is prohibited.\>

* \<Remote access sessions must be configured to enforce timeout after a specified period of \<X hours\>.\>

* \<Remote-access technologies for vendors and business partners used to access production systems must be enabled only when needed for business purposes and immediately deactivated after use.\>

* \<Any hybrid networks with both cloud and on-premise access shall be scanned and tested at least annually to ensure that security requirements are maintained.[^18]\>

* \<OTHER COMPANY SPECIFIC REQUIREMENTS\>

I. Cloud Hardening

1\. Identity and Access Management (IAM)

* Least Privilege Principle: Ensure each entity (user, service, system) possesses minimal necessary access.  
* Enforce Multi-Factor Authentication (MFA) for production access

2\. Data Storage and Management

* Data Encryption: Ensure encryption for data at rest and in transit in accordance with the *Cryptography Policy*  
* \[Optional if requiring VPN\] Private Endpoints: Enable private endpoints and VPNs to safeguard against data interception.  
* Data Lifecycle Management: Configure backups for customer data repositories.

3\. Network Security

* Isolation: Utilize VPC and subnets to isolate environments and segment networks.  
* Firewalls: Implement cloud-native or third-party firewall solutions and DDoS protection services.

4\. Monitoring and Logging

* Logging: Configure logging focusing on write-once-read-many storage to prevent tampering.  
* Alerting: Implement cloud-based alerting (Amazon CloudWatch, Azure Alerts) for real-time incident response.

II. Container Hardening

1\. Image Security

* Secure Source Image: Create images only from \<Company Name\>\-authorized base images or repositories  
* Minimalist Design: Adopt minimal base images to reduce attack vectors.

2\. Runtime Security

Runtime Analysis: Implement runtime security tools for live vulnerability and threat detection.

3\. Network Security

Policy-Based Controls: Implement network policies using third party or cloud native tools.

4\. Orchestration Security

* API Server: Shield the API server with appropriate firewalls, IAM controls, and secure communication channels.  
* RBAC: Establish and periodically review orchestration access privileges, ensuring conformance to the least privilege principle.

5\. CI/CD Security

Pipeline Access: Minimize access to CI/CD pipelines, employing role-based access controls and audit trails.

* Dependency Scanning: Scan for vulnerable dependencies during build processes

III. Servers and Virtual Machines

Baseline Configuration

* Ensure systems are aligned with industry-standard baselines (CIS Benchmarks, NIST Guidelines).

Technical Adherence

* Vendor Defaults: All default configurations, especially passwords, must be altered prior to network integration.  
* Role Specialization: Maintain a singular primary function per VM to uphold segregation of duties and reduce lateral movement opportunities.  
* Patch Management: Establish a patch management strategy to meet defined SLAs.

IV. Network Standards

Network Management and Documentation

* Change Management: Any alterations to network settings must adhere to the change management processes.

Traffic Management in Production Environments

* Rule Enforcement: Strictly enforce predefined rules, which should be revisited and validated at least annually.  
* Remote Access Control: Ensure strict control and auditing of remote access, restricting and logging all connections.

NACLs and Traffic Control

* Establish stringent rules governing traffic in accordance with a define business justification

[^1]:  All fields in this document marked by angled brackets \< \> and highlighted must be filled in.

[^2]:  Describe your company’s policy for segregation of environments. If you use different categorizations of data (i.e., don’t use “confidential”), then make sure to update those references here.

[^3]:  This is a reference to another Vanta policy. If you are not using this policy, describe how “confidential” data is here.

[^4]:  This is a reference to an appendix included in this document. If you are not using the appendix, remove this reference. Either describe your configuration and hardening standards here or reference another document.

[^5]:  Documented backup procedures should be referenced, added in the Appendix or this policy language should be tailored.

[^6]:  Segregation of backups policy added for v2

[^7]:  Backup restore test policy added for v2

[^8]:  Logging content policy added for v2. Aligned to MVSP. Modify as needed.

[^9]:  Restore logs added for v2

[^10]:  Remove these paragraphs if your company does not have a file integrity monitoring and intrusion detection-related control.

[^11]:  Tailor this language to your environment

[^12]:  Update this table to describe your company’s vulnerability remediation commitments. Some organizations may set different policies based on system or network type. For example, external-facing systems are required to be patched more quickly than internal systems. If a policy like this exists within your organization, detail it here.

[^13]:  This is a reference to another Vanta policy. If you are not using that policy, describe your company’s policy for the installation of software by users here.

[^14]:  Reference to another Vanta Policy. Tailor as needed.

[^15]:  Include a link to your company’s wiki page about your company’s configuration and hardening standards. If you do not have a wiki, describe the standards here.

[^16]:  Template for hardening. Modify as needed.

[^17]:  Delete if N/A

[^18]:  ISO 27017