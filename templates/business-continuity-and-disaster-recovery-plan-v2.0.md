**Vanta policy template instructions**

This Vanta policy template represents a complete, compliance-ready policy with placeholders for company specific text. Each policy section represents a policy-specific topic that you should consider and/or modify to match your company’s practices.

**For each policy section**

* Consider if this section and its corresponding risks applies to you. If it does not, remove it and/or replace it with your organization’s corresponding practices.  
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

A good rule-of-thumb is to keep your language high enough level such that it stays representative for at least a year. If you have more questions about how to use this template, please reach out to [support@vanta.com](mailto:support@vanta.com) or your auditor for additional guidance.

# **Business Continuity and Disaster Recovery (BC/DR)[^2]**

**Policy Owner:** \<Policy owner\>

**Effective Date:** \<Effective date\>

# **Purpose**

The purpose of this business continuity plan is to prepare \<Company Name\> in the event of service outages caused by factors beyond our control (e.g., natural disasters, man-made events), and to restore services to the widest extent possible in a minimum time frame. 

# **Scope**  

All \<Company Name\> IT systems that are business critical. This policy applies to all employees of \<Company Name\> and to all relevant external parties, including but not limited to \<Company Name\> consultants and contractors.

The following scenarios are excluded from the BC/DR plan scope[^3]:

* Loss of availability for a production hosting service provider (i.e., \<production hosting service provider, e.g., AWS\>)  
* Loss of availability of \<Company Name\> satellite offices (these will be considered incidents)

In the event of a loss of availability of a hosting service provider, the \<driver of the response, e.g., VP of Global Support\> will confer with the \<assistants for the response, e.g., IT Manager and executive staff\> to determine an appropriate response strategy[^4].

# **Policy**

In the event of a major disruption to production services and a disaster affecting the availability and/or security of the \<Company Name\> office, senior managers and executive staff shall determine mitigation actions.

A disaster recovery test, including a test of backup restoration processes, shall be performed on an annual basis.

Continuity of information security shall be considered along with operational continuity.

In the case of an information security event or incident, refer to the Incident Response Plan[^5].

# **Alternate Work Facilities**

If the \<Company Name\> office becomes unavailable due to a disaster, all staff shall work remotely from their homes or any safe location.

# **Communications and Escalation**

Executive staff and senior managers should be notified of any disaster affecting \<Company Name\> facilities or operations.

Communications shall take place over any available regular channels including \<list your company’s regular communication channels, e.g., Slack, email, phone and online meeting tools\>.

Key contacts shall be maintained on the on-call schedule and key contacts: \<link to wiki page that lists out key contacts\>[^6]

# **Roles and Responsibilities[^7]**

| Role | Responsibility |
| :---- | :---- |
| \<IT Manager\> | The IT Manager shall lead BC/DR efforts to mitigate losses and recover the corporate network and information systems. |
| \<Departmental Heads\> | Each department head shall be responsible for communications with their departmental staff and any actions needed to maintain continuity of their business functions. Departmental heads shall communicate regularly with executive staff and the IT Manager. |
| \<Managers\>  | Managers shall be responsible for communicating with their direct reports and providing any needed assistance for staff to continue working from alternative locations. |
| \<VP of Global Support\>  | The VP of Global Support, in conjunction with the CEO and CFO shall be responsible for any external and client communications regarding any disaster or business continuity actions that are relevant to customers and third parties. |
| \<VP of Engineering\> | The VP of Engineering, in conjunction with the VP of Global Support, shall be responsible for leading efforts to maintain continuity of \<Company Name\> services to customers during a disaster. |
| \<Chief HR Officer\> | The CHRO shall be responsible for internal communications to employees as well as any action needed to maintain physical health and safety of the workforce. The CHRO shall work with the IT Manager to ensure continuity of physical security at the \<Company Name\> office. |

# **Continuity of Critical Services**

Procedures for maintaining continuity of critical services in a disaster can be found in Appendix A[^8].

Recovery Time Objectives (RTO) and Recovery Point Objects (RPO) can be found in Appendix B[^9].

Strategy for maintaining continuity of services can be seen in the following table[^10]:

| KEY BUSINESS PROCESS | CONTINUITY STRATEGY |
| :---- | :---- |
| Customer (Production) Service Delivery | Rely on AWS availability commitments and SLAs |
| IT Operations | Not dependent on HQ. VPN is redundant between HQ and Colo. Critical data is backed up to alternate locations. |
| Email | Utilize Gmail and its distributed nature, rely on Google’s standard service level agreements. |
| Finance, Legal and HR | All systems are vendor-hosted SaaS applications. |
| Sales and Marketing | All systems are vendor-hosted SaaS applications. |

### **Plan Activation**

### **This BC/DR shall be automatically activated in the event of the loss or unavailability of the \<Company Name\> office, or a natural disaster (i.e., severe weather, regional power outage, earthquake) affecting the larger \<describe the location of your company’s headquarters, e.g., San Francisco, CA\> region.**

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :---: | :---: | :---: |
| \<1.0\> | \<29-Apr-2020\> | \<First Version\> | \<OWNER\> | \<APPROVER\> |
|  |  |  |  |  |

# **Appendix A – Business Continuity Procedures by Scenario[^11]**

## **Business Continuity Scenarios**

### **HQ Offline (power and/or network)**

* CRM, Telephony, Video Conferencing/Screen Share & Corp Email unaffected  
* SUPPORT unaffected  
* HQ Staff offline (30-60 minutes)  
* Remote Staff unaffected (US)

#### ***Procedure:***

1. HQ Staff relocate to home offices (30-60 minutes)  
2. Verify Telephony, CRM, & Email Connectivity at home offices (10 minutes)  
3. Remotely resume normal operations 

### **Colo Offline (power and/or network)**

* CRM, Telephony, Video Conferencing/Screen Share & Corp Email unaffected  
* SUPPORT Offline  
* Production Database offline (redundant)  
* HQ Staff unaffected  
* Remote Staff unaffected (US)

#### ***Procedure:***

1. Notify Customer Base that proactive monitoring is offline  
2. Normal operations continue

### **Disaster Event at HQ (\<Location 1\> & \<Location 2\>)**

* CRM, Telephony, Video Conferencing/Screen Share & Corp Email unaffected  
* SUPPORT offline  
* HQ Staff offline (variable impact)  
* Remote Staff unaffected (US)

#### ***Procedure:***

3. Activate Remote Staff (US)  
4. Notify Customer Base of impaired functions & potential delays  
5. Commandeer Field Resources for Critical Response (SE Teams)

### **SaaS Tools Down**

* CRM, Telephony, Video Conferencing/Screen Share, or Corp Email Affected  
* SUPPORT partially affected (no new cases, manual triage required)  
* HQ Staff unaffected  
* Remote Staff unaffected (US)

#### ***Procedures:***

##### *Telephony Down* 

1. Notify Customer Base to use Support Portal or Email  
2. Support Staff use Mobile Phones and/or Land Lines as needed

##### *Email Down (Gmail/Corp Email)*

1. Support Staff manually manage ‘case’ related communications  
2. Support Staff use alternate email accounts as needed (Hotmail)

##### *CRM Down*

1. Notify Customer Base that CRM is down  
2. Activate ‘Spreadsheet’ Case Tracking (Google Sheets)  
3. Leverage ‘Production’ Database for Entitlements, Case History, Configuration data.

##### *Video Conferencing/ScreenShare Down (Zoom)*

4. Support Staff utilize alternate service as needed

# **Appendix B – RTOs/RPOs[^12]**

| Rank | Asset | Affected Assets | Business Impact | Users | Owners | Recovery Time Objective (RTO) | Recovery Point Objective (RPO) | Comments / Gaps |
| :---: | ----- | ----- | ----- | ----- | ----- | :---: | :---: | ----- |
| 1 | Google Datacenters | Site | Core services | All | Engineering |  |  |  |
| 2 | Corporate Office | Site | Inability to access data? Any other impacts? | All | IT Ops |  |  |  |
|  | Corporate Network | Network | Inability to use network resources from corporate office | All | IT Ops |  |  |  |
|  | Google Cloud | Network | Core services | All | Engineering |  |  |  |
|  | Home Office ISP Networks | Network |  | IT Ops, Development | N/A |  |  |  |
|  | Subcontractor Networks | Network |  | Development | N/A |  |  |  |
|  | Third Party Networks | Network |  | Sales | N/A |  |  |  |
|  | Company Laptops | Hardware |  | All | IT Ops |  |  |  |
|  | Digital Projector | Hardware |  | All | IT Ops |  |  |  |
|  | Office Printers | Hardware | Inability to print in corporate office | All | IT Ops |  |  |  |
|  | Personal Mobile Device | Hardware |  |  |  |  |  |  |
|  | Wireless Access Points (WAP) | Hardware |  | All | IT Ops |  |  |  |

[^1]:  All fields in this document marked by angled brackets \< \> and highlighted must be filled in.

[^2]:  BC/DR Policies and Plans differ significantly between different organizations. If you have an existing plan that works you should consider keeping it. You can also find other examples and templates. Pick what works best for your organization.

[^3]:  Exclusions to this policy should be customized to your organization. Your company may not have any exclusions in which case you can remove this language. These scenarios are provided as an example.

[^4]:  Change or remove this language based on your organization’s needs.

[^5]:  This is a reference to another Vanta document. If you are not planning on using this document, describe how your company will respond to an information security event or incident here. It is, however, highly recommended that your organization has an Incident Response Plan because a managed approach to incident response is a requirement for all information security management standards.

[^6]:  If your company does not use a wiki or some form of an internal knowledge base that can be linked here, you can list out the key contacts in this document. If you list out the contacts here, however, you will need to continually update this document and your employees may have to re-accept this policy if there are major changes.

[^7]:  Adjust this table of roles and responsibilities to describe the roles and responsibilities for members of the BC/DR team

[^8]:  This references an appendix in this document. If you describe these procedures elsewhere, update this reference.

[^9]:  RTO/RPO Table added to Appendix B for v2

[^10]:  Adjust the table below the describe your company’s continuity strategies

[^11]:  In this appendix, describe your company’s business continuity procedures. The scenarios listed in this table are examples of what you might consider including.

[^12]:  Customize for your business