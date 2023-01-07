# [ORGANISATION] SECURITY PROGRAMME

## 1. Programme Overview
We are excited to announce that [ORGANISATION] has completed the annual third party audit of our Information Security Management System (ISMS) and has achieved the ISO/IEC 27001:2013 certification for all our SaaS products. ISO 27001 is an industry standard for information security. This also means that we have discontinued pursuing our SOC2 type 2 and Cyber Essentials certifications. The British Standards Institution has affirmed that whichever [ORGANISATION] product you use, this will be in compliance with ISO 27001:2013. For our customers, this means that the products you use are safely operating under the requirements of ISO 27001 and that all data is processed accordingly. In case of questions regarding this kindly reach out to your customer success manager.

[ORGANISATION] maintains a comprehensive security programme to support regulatory compliance, preserve customer trust, and safeguard the security, privacy, confidentiality, integrity, and availability of systems processing confidential information. The [ORGANISATION] security team is staffed by dedicated professionals reporting directly to executive management and our board of directors. All [ORGANISATION] products are ISO 27001:2013 certified. We engage a third party to audit our adherence to these standards at least annually. Our current ISO 27001 certificate is available upon request.

[ORGANISATION] provides a suite of products and services under two solution groups, on one hand Media Intelligence, that includes our flagship product LI2 and [ORGANISATION] Reviews, and on the other hand Social Media Management which is comprised of Publish, Listen, Audience, Engage, Measure, Advertise, Benchmark and Influence.

All [ORGANISATION] employees receive information about our policies and procedures as they relate to security and data privacy. [ORGANISATION] employees must review and sign an Acceptable Use Policy and undergo security and data privacy training upon hire and at least annually thereafter. [ORGANISATION] performs background and/or reference checks for all new hires according to local laws and regulations as a condition of hire.

## 2. Data Centres and Third Party Hosting
The different components of the [ORGANISATION] product suite are hosted across a variety of services in order to take advantage of the benefits of different classes of infrastructure and ensure continuous, uninterrupted availability of the platform. Each of these service providers are held to the same standards we hold ourselves, and we assess their security practices annually.

We make extensive use of [CLOUD-PROVIDER] e.g Amazon Web Services (AWS). For business continuity and recovery, raw data ingestion, indexing, analysis, and storage takes place in [CLOUD-PROVIDER] in the [COUNTRY]. AWS is certified to a wide range of compliance and security standards, available for review [here](https://aws.amazon.com/compliance/programs/). 

The BCR frontend applications and LI2 components are hosted in Google Cloud Platform (GCP) Europe. As with AWS, GCP has a variety of certifications, viewable here.

Analysis results and customer metadata are stored in colocation facilities in the UK. The primary data centre is in Hayes, UK, with services provided by [Virtus DC](https://virtusdatacentres.com/services/security). The backup data centre is in Maidstone, UK, with services provided by [Custodian DC](https://www.custodiandc.com/resources/factsheets). Both data centre providers manage Tier III or better facilities with 24/7 on-site security personnel and extensive physical security controls.

The LI2 platform is hosted in AWS and GCP in the EU (see links above for compliance information) except for the infrastructure used to support the Listening product which is hosted in the US and the UK, but contains public information only (public Tweets, blog articles, Facebook posts etc.)

Paladin is hosted in Heroku and AWS in the US.

We supplement the above services with small presences in Linode and Aiven.

## 3. Access Control and Data Protection
### Platform access control
We have implemented strict user roles in our products to allow our customers control and flexibility over what features their users can access. We believe it is necessary to give all of our customers this level of flexibility, as the requirements for access control are different in every organisation.

Users of the Consumer Research and any of the products in the Social Media Management solution with the Admin user type can manage all user roles and permissions for their teams. For more detailed instructions regarding user permissions within our applications, please refer to the [ORGANISATION] Help Center and the Falcon Help Center.

### Internal access to customer data
We limit customer instance access to only [ORGANISATION] Group employees who require access to service a given customer account, such as account managers and customer support personnel. We audit all access monthly, quarterly, or annually depending on the level of access and the sensitivity of the data involved.

Remote access to server infrastructure is limited to engineering personnel with a demonstrated business need for access using the principle of least privilege. Access requests are ticketed, reviewed, and approved by senior management and the security team, and then reviewed quarterly. In order to access systems containing customer information, [ORGANISATION] employees must authenticate via a VPN, and provide a physical access token as a second factor.

### Physical access control
As mentioned, [ORGANISATION] does not rely on physical locations to process customer data. However, we have implemented a series of controls to manage physical access to our offices. Where possible, our offices have front desk personnel assigned to monitor access. All visitors must check in and out, and be accompanied by a [ORGANISATION] employee throughout their visit. All [ORGANISATION] employees have keycards to access offices. Where front desk personnel are unavailable, entry doors to office space are kept locked.

### Separation of platform data
The [ORGANISATION] Group’s products are multi-tenant SaaS applications. We logically separate customer data through database design, coding standards, and thorough code reviews. Each user and piece of data within the products includes a unique identifier. We bind every user session to a user identifier, which is then used to retrieve data. Each user is granted a set of permissions, which then dictates access within the product(s). We never use customer data during our development or testing processes (with the exception of Influence, which is moving away from this soon). The production environment is logically segregated from all non-production environments.

### Encryption
We encrypt all [ORGANISATION] issued employee computers with the full disk encryption offered by the operating system used. Windows machines use Bitlocker, Apple devices use Filevault 2, and Linux devices use dm-crypt with LUKS.

We encrypt all customer uploaded data and login credentials in transit. All communication with the [ORGANISATION] Group’s products occurs over HTTPS. The products support TLS 1.2, and 1.3 protocols and use TLS 1.2 by default for all data in transit over HTTPS for browsers that support it.

Custom uploaded data and related backups are encrypted at rest using Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3). Physical backup tapes from our data centres are encrypted with AES-256.

Additionally, all data in the Falcon platform and Paladin is encrypted at rest.

### Data retention and deletion
Unless otherwise noted in your contract, if you terminate your contract with [ORGANISATION], we will retain your data for a maximum of 30 days. After the 30-day window, with the exception of any information that we are legally required to retain, an automated process deletes or anonymizes all data in the platform related to the expired contract.

### Single Sign-on, Password Security, and MFA
For [ORGANISATION] Consumer Research, Single Sign-on (SSO) via SAML 2.0 and Google Authentication are offered to certain customers as a premium feature. Both types of SSO offer configuration settings to authenticate via SSO only, or the ability to authenticate via SSO or standard email and password authentication. At the present time, we do not offer account provisioning via SSO BCR. All accounts must be created through the administration area.

Passwords are one-way hashed and salted using bcrypt. Our minimum requirement for passwords is 8 characters, 1 numeric and special character. The platform features optional Automatic Password Expiry. With Automatic Password Expiry enabled, users will be required to change their password every 90 days. Users are restricted from accessing the platform if they fail to enter the correct password 10 times in a row.

The products in the Social Media Management solution support a wide range of authentication methods to keep your social media content safe and secure. In addition to email/password, two-factor authentication (2FA), single sign-on (SSO) through Google, Facebook, Twitter, and LinkedIn, we allow our customers to use their own Identity Provider (IdP) to authenticate their users. The external providers supported are SAML and OpenId Connect. This is included with no additional costs.

For these products, passwords must be at least 8 characters, it must not match any of the last 3 passwords which were created for that user, there are no minimum requirements for a particular character type and the password must not consist of a word, phrase, or sequence which is too generic or common.

Access to Influence is protected by complex password controls and two-factor authentication.

[ORGANISATION] employees must use a password manager and generate unique, sufficiently complex passwords for all services accessed. We do not currently place any further restrictions on passwords as recent guidelines (see: https://github.com/usnistgov/800-63-3) advise against overly complex requirements.

For service accounts, we do not generally use passwords and instead rely on other methods for access (SSH keys, MFA, hardware tokens). We require the use of multi-factor authentication for all [ORGANISATION] Group employee user accounts. We do not currently offer MFA for end users.

## 4. Device and Network Security
### Endpoint security
All endpoints are protected by Endpoint Detection and Response software. [ORGANISATION] employees do not receive privileged access to their machines unless there is a clear business need for them to have it. Employees with elevated access must commit to additional security requirements in order to receive this level of access.

Devices are monitored and managed using a mobile device management (MDM) system. All company laptops and phones may be remotely wiped in the event they are lost or stolen. [ORGANISATION] employee devices all use the native full disk encryption available for their operating system: FileVault for Mac OS, BitLocker for Windows 10, and LUKS for Linux.

Company wireless networks do not provide access to sensitive systems.

### Server and network security
[ORGANISATION] Consumer Research and Social Media Management servers are managed via configuration management software, and changes to configuration standards are monitored and audited periodically. Physical servers in our colocation centres are hardened according to a security checklist during provisioning. Cloud instances are monitored using cloud monitoring tools designed to detect anomalous activity and deviation from standards. All hosting infrastructure is only available from through a VPN, requiring MFA for authentication.

We use honeypots and other network monitoring tools to detect and prevent intrusion or other unwanted behaviour. Server logs are shipped to a central logging service and managed by a dedicated monitoring team. Logs are retained for 2 to 6 months depending on their purpose. Log files contain a wide variety of information, including but not limited to privilege escalations, actions taken as root, and user access patterns.

Audit logs that keep records on who performed an action on which entity and when are made available to customers for Social Media Management, please refer to this page for more information. Logs are kept for the duration of the client’s contractual agreement.

[ORGANISATION] Influence currently runs on manually configured servers but we are working on implementing Infrastructure as Code best practices.

## 5. Business Continuity, Disaster Recovery, and SLAs
[ORGANISATION] does not rely on physical locations to provide services, therefore our exposure to most threats of disaster is minimal. However, we do have an extensive business continuity policy and incident response procedure for most of our products (Consumer Research, Audiences and Vizia). This policy includes established roles for incident response and a dedicated emergency response team made up of high-level employees from across the organisation and our geographic locations. 

We have informal processes and procedures for all other products which we are working on formalising.

All critical infrastructure components are redundant. For cloud services on most of our products (Consumer Research and Social Management Suite), we load balance our servers across multiple availability zones and our databases live in multiple availability zones. Cloud data backups are stored in separate doomsday vault accounts. For physical infrastructure, we maintain two data centers and perform daily backups. Weekly backups are also taken and stored by a third party service provider in the form of encrypted backup tapes.

Our engineering teams maintain documented standard operating procedures and runbooks to address a variety of scenarios. Engineering teams run backup restoration tests for critical services at least annually. We have also implemented an on-call rotation to ensure 24/7 coverage of our systems in the event of an incident.

For more information on our uptime commitments, please review our Service Level Agreement document.

### Recovery Point Objectives (RPO)
[ORGANISATION] Consumer Research systems have an RPO of 24 hours maximum, meaning that at the worst case, no more than 24 hours of data are lost and valid backups are taken at least every 24 hours. Specific products may have shorter duration RPOs depending on backup practice and/or technology choice. RPO may be as little as a few seconds in the case of some critical systems.

### Recovery Time Objectives (RTO)
The majority of [ORGANISATION] Group products have an RTO of less than one business day. There are two potential exceptions to this RTO:

Ongoing and critical failure of any of our critical services vendors. It could take up to a month to await system recovery or switch to an alternative vendor, however, contingency plans in place can bring the business back to an operational status in 24 to 48 hours in the absence of one of those systems.

Complete loss of primary social media archives. In the event of such a failure, minimum functionality could return almost immediately, with coverage expanding rapidly. However, given the amount of data involved in rebuilding these archives, full recovery could take days, if not weeks.

## 6. Security in Development
### Quality control and change management
We follow a strict quality protocol during the development, testing, and deployment of our software updates. During the design phase of all [ORGANISATION] Group features, stakeholders from various departments examine detailed test cases to make sure that the feature will meet the necessary requirements. We also incorporate user testing whenever possible to ensure that our product most accurately meets the needs of our customers.

All code released to production has been reviewed and tested by our Quality Assurance teams or automated tests and by senior engineers who did not directly work on the code in question. We use git for version control, and GitHub for source code hosting. All releases follow a specific protocol and all actions taken during a release are logged to GitHub and relevant internal documentation channels.

Engineers are provided security training and documentation on a regular basis, including periodic refresher training on the OWASP Top 10.

### Vulnerability and penetration testing
We perform vulnerability testing at least monthly, and engage a third party to perform intensive manual and automated penetration and web application testing annually. Our most recent test results are available on request under a Non Disclosure Agreement.

## 7. Vendor and Contractor Security
Our security, IT, and privacy teams review all vendors prior to purchasing software or services, and annually or upon renewal thereafter. Reviews include an assessment against security standards, data handling and privacy requirements, and suitability for business use.

[ORGANISATION] uses contract employees for two primary purposes: foreign language social media support and software development services. In the former case, contractors are required when a customer requests data or reports in languages not directly supported by [ORGANISATION] employees. In the latter case, the [ORGANISATION] Group has maintained long-term relationships with small groups of contract software developers. These contractors provide feature development support and are fully integrated into our secure development lifecycle. All contractors sign non-disclosure agreements and our acceptable use policy. Contractor access to customer data is limited to the minimum access required to perform their duties.

## 8. Data Breach Notification
The [ORGANISATION] Group commits to notifying affected entities without undue delay and in any event within 36 hours after becoming aware of a data breach (as defined in Data Protection Legislation requirements).

## 9. Compliance
For details regarding how we fulfill our data privacy, legal, and regulatory compliance obligations, please visit the Legal and Privacy sections of this website.

## 10. Vulnerability Disclosure
We do not have an official bug bounty programme (nor do we expect to create one in the near future). This means we do not have standing financial or personnel resources dedicated to handling unsolicited bug reports. That said, we are happy to accept and triage submissions to security@brandwatch.com, and we may choose to provide compensation for these submissions where appropriate. Vulnerabilities found are not confidential, but we would ask that you not publicly disclose the things you find without giving us time to remedy any issues. We will do our best to provide valid findings with appropriate compensation. However, please keep in mind that our assessment of what’s appropriate may differ from yours, and we unfortunately cannot negotiate reward amounts.

## 11. Feedback
We capture customer concerns and feedback within all of our products using Intercom (www.intercom.com). You can get in touch with the [ORGANISATION] Product Support team via the [ORGANISATION] Help Center (support.brandwatch.com). To access either Intercom or the [ORGANISATION] Help Center, you must be logged in to the product. Customers may also contact their Customer Success Manager directly.

If you would like additional information on the features and functionality of [ORGANISATION], please reach out to our Sales or Services teams. For specific security, privacy, or compliance related issues, please contact security@brandwatch.com or privacy@brandwatch.com.
