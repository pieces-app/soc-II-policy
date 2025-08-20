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

# **Secure Development Policy** 	 

**Policy Owner:** \<Policy owner\>

**Effective Date:** \<Effective date\>

# **Purpose** 

To ensure that information security is designed and implemented within the development lifecycle for applications and information systems.

# **Scope**

All \<Company Name\> applications and information systems that are business critical and/or process, store, or transmit Confidential data. This policy applies to all internal and external engineers and developers of \<Company Name\> software and infrastructure.

# **Policy**

This policy describes the rules for the acquisition and development of software and systems that shall be applied to developments within the \<Company Name\> organization.

# **System Change Control Procedures[^2]**	

Changes to systems within the development lifecycle shall be controlled by the use of formal change control procedures. Change control procedures and requirements are described in the \<Company Name\> Operations Security Policy. 

Significant code changes must be reviewed and approved by \<who can approve code changes, e.g., a developer or manager within the Review Board\> before being merged into any production branch in accordance with the \<name of process, e.g., Check In Process\> found here: \<link to process outline in company wiki\> 

Change control procedures shall ensure that development, testing and deployment of changes shall not be performed by a single individual without approval and oversight.

# **Software Version Control[^3]**	

All \<Company Name\> software is version controlled and synced between contributors (developers). Access to the central repository is restricted based on an employee’s role. All code is written, tested, and saved in a local repository before being synced to the origin repository.

# **Technical Review of Applications after Operating Platform Changes**	

When operating platforms are changed, business critical applications shall be reviewed and tested to ensure that there is no adverse impact on organizational operations or security.

# **Restrictions on Changes to Software Packages**	

Modifications to third-party business application packages shall be discouraged, limited to necessary changes and all changes shall be strictly controlled.

# **Secure System Engineering Principles**	

Principles for engineering secure systems shall be established, documented, maintained and applied to any information system implementation efforts.

At a minimum, the following secure-by-design and privacy-by-design principles shall be applied[^4]:

Secure-by-design principles:

1. Minimize attack surface area  
2. Establish secure defaults  
3. The principle of Least privilege  
4. The principle of defense in depth  
5. Fail securely  
6. Don’t trust services  
7. Separation of duties  
8. Avoid security by obscurity  
9. Keep security simple  
10. Fix security issues correctly

Privacy-by-design principles:

1. Proactive not Reactive; Preventative not Remedial  
2. Privacy as the Default Setting  
3. Privacy Embedded into Design  
4. Full Functionality – Positive-Sum, not Zero-Sum  
5. End-to-End Security – Full Lifecycle Protection  
6. Visibility and Transparency – Keep it Open  
7. Respect for User Privacy – Keep it User-Centric

Engineering documentation and technical references can be found in the \<name of page with documents, e.g., Development Process Confluence Page\> here: \<link\>

Software developers are expected to adhere to \<Company Name\>’s coding standards throughout the development cycle, including standards for quality, commenting, and security. 

# **Secure Development Environment[^5]**	

\<Company Name\> shall establish and appropriately protect environments for system development and integration efforts that cover the entire system development life cycle. The following environments shall be logically or physically segregated:

* Production  
* Test / Staging  
* Development

# **Outsourced Development[^6]**	

\<Company Name\> shall supervise and monitor the activity of outsourced system development. Outsourced development shall adhere to all \<Company Name\> standards and policies. 

# **System Security Testing**	

Testing of security functionality shall be performed at defined periods during the development life cycle. No code shall be deployed to \<Company Name\> production systems without documented, successful test results and evidence of security remediation activities. 

# **Application Vulnerability Management[^7]**	

Application code should be scanned prior to deployment. Patches to address application vulnerabilities that materially impact security should be deployed within 90 days of discovery.

# **System Acceptance Testing[^8]**

Acceptance testing programs and related criteria shall be established for new information systems, upgrades and new versions.

Prior to deploying code, a Release Checklist MUST be completed which includes a checklist of all Test Plans which show the completion of all associated tests and remediation of identified issues.

# **Protection of Test Data**	

Test data shall be selected carefully, protected and controlled. Confidential customer data shall be protected in accordance with all contracts and commitments. Customer data shall not be used for testing purposes without the explicit permission of the data owner and the \<approver of use of customer data as test data, e.g., VP of Engineering\>.

# **Acquisition of Third-Party Systems and Software**

The acquisition of third-party systems and software shall be done in accordance with the requirements of the \<Company Name\> Third-Party Management Policy[^9].

# **Developer Training[^10]**

Software developers shall be provided with secure development training appropriate to their role at least annually. Training content shall be determined by management but shall address the prevention of common web application attacks and vulnerabilities. The following threats and vulnerabilities should be addressed as appropriate:

* prevention of authorization bypass attacks  
* prevention of the use of insecure session IDs  
* prevention of Injection attacks  
* prevention of cross-site scripting attacks  
* prevention of cross-site request forgery attacks  
* prevention of the use of vulnerable libraries

# **Exceptions**

Requests for an exception to this Policy must be submitted to the \<approver of exceptions to this policy, e.g., VP of Engineering\> for approval.

# **Violations & Enforcement**

Any known violations of this policy should be reported to the \<receiver of reported violations to this policy, e.g., VP of Engineering\>. Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :---: | :---: | :---: |
| \<1.0\> | \<29-Apr-2020\> | \<First Version\> | \<OWNER\> | \<APPROVER\> |
|  |  |  |  |  |

[^1]:  All fields in this document marked by angled brackets \< \> and highlighted must be filled in.

[^2]:  This is a reference to another Vanta policy. If you are not planning on using this policy, describe your company’s change control procedures and requirements here.

[^3]:  Describe your company’s version control use here

[^4]:  Security and privacy by design principles added for v2

[^5]:  Tailor this section to describe your company’s development environment and SDLC

[^6]:  This section references outsourced development. If you company does not use outsourced development, remove this section.

[^7]:  Application vulnerability management added for v2

[^8]:  Describe your company’s acceptance testing process here

[^9]:  This is a reference to another Vanta policy. If you are not planning on using this policy, describe your company’s third-party systems and software acquisition processes

[^10]:  Developer training added v2