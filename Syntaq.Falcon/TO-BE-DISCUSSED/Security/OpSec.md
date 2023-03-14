This section outlines the steps taken by SYNTAQ in Design, Development and Deployment stages of the application lifecycle to ensure maximum security and reliability of its services. SYNTAQ's repertoire of OpSec practices covers a full spectrum, starting with on-prem and physical security concerns, all the way to shoring up defenses on the Cloud, and having in place a practical Disaster Recovery Plan. 

These are all an integral part of SYNTAQ's Business Continuity Plan provided to our clients. 

* This document references and supports Syntaq Falcon Application Security Overview v1.0.0 which discusses in detail the specific security features of SYNTAQ Falcon app. 

# Software-as-a-Service and Operational Security 

Security is one of the main pillars of any software application, especially so when you are dealing with a piece of software that delivers high-value services and handles sensitive data. Syntaq, as a cloud-based SaaS, relies, in part, on the prowess of Microsoft as the provider of Azure cloud services on which it is hosted. But service providers in the cloud work based on a shared-responsibility model which requires the consumers of those services to take charge of securing their systems vis-a-vis configuration settings, access management, roles, etc.  

Thus, there are several industry-standard best practices Syntaq adheres to strictly to ensure a continuous and secure service. Furthermore, Syntaq, as a multi-tenant service application, advises its clients on security measures and the proper use of the system.  

Below is a list of some of the provisions built into the application to minimize the effort required on the part of the end-users to operate at optimum security level (for a full description refer to Syntaq Falcon Application Security Overview v1.0.0): 
- In-depth Authorization system integrated as part of the application’s code 

- Periodic review of protection logic in source code 
- User and Role management pages for Administrators 
- Teams feature to provide group policies (permissions) 
- Automatic Cross-Site Request Forgery protection 
- Two factor authentication 
- Password complexity settings 
- User Lockout and logging feature 

Beyond that, and on the deployment level, Syntaq takes an active part in ensuring a comprehensive security package to complement Microsoft Azure's out-of-the-box features. These areas include: 
- Physical security 
- General security policies 
- Identity and Access Management (IAM) 
- Manage access to resources (storage accounts) 
- Data access management (database) 
- Virtual machines 

# Physical Security 
With regards to on-prem security, Syntaq educates its employees on the appropriate security measures and maintains a strict monitoring and logging discipline. Access to Syntaq facilities is secured by means of electronic passkeys, locked out to unauthorized traffic. The workstations are built on robust hardware, regularly maintained and upgraded, and monitored for fraudulent activity. Admins in charge of these workstations are required to use complex passwords and multi-factor authentication (where applicable), and to review and change those passwords periodically.  
- Use tools like last pass to store/ secure passwords 
- Enforcing the use of secure pass keys to access the offices 
- Applying the least-privilege principle for user and admin access  
- Continuous surveillance of on-site personnel   
- Restricting USB ports on workstations to avoid malware insertion/theft  

# Security Policies 
This is where the proper configuration of settings come into play. Overlooking the settings as “trivial” or relying on the default settings is a mistake that could come back to haunt your application in the long run. To avoid this as much as possible, Syntaq employs the following best practices:
- Continuous system updates 
- Using Microsoft Monitoring Agent which provides alerts and scans for various security-related configurations on Azure virtual machines 
- Just-in-time VM access - locks inbound traffic on selected ports 
- Enabling SQL auditing & threat detection 
- Using SQL encryption on Azure SQL Database, associated backups, and transaction log files 
- Enabling OS vulnerabilities recommendations 
- Enabling endpoint protection recommendations 
- Using disk encryption feature 
- Utilizing Network Security Groups 
- Web Application Firewall (where applicable) 
- Next-Generation Firewall set to ‘on’ 
- Security alerts for email and phone 
- Minimizing the number of admins/owners 
- Deleting deprecated/unused accounts 

# Identity and Access Management 
Having the best encryption methods and the most advanced firewall is of no use if authorized access to your application and its resources is compromised. You do not want to build the most secure door ever and then lose the key!  

To that end, Syntaq implements strict Identity and Access Management policies, as outlined below: 
- Enabling multi-factor authentication for all users with Write permission  
- No guest users allowed (unless necessary) 
- Users NOT allowed to remember multi-factor authentication on devices (trusted devices) 
- Methods required to reset passwords set to 2 
- Users must re-confirm their authentication information on regular basis 
- Notifying users of password resets 
- Notifying admins of other admins’ change of credentials 
- Applying the Least Privilege Principal 
- Restricting access to Azure Active Directory administration portal to fewest possible admins 
- Restricting security management access to fewest possible admins  

# Resource Access Management 
Syntaq’s criteria for data protection, as per Azure best practices, are as follows: 
- Secure transfer - Enabling data encryption in transit: Access to storage accounts must be through HTTPS. Any requests using HTTP, SMB or other protocols will be rejected 
- Storage service encryption - Enable data encryption at rest for blobs: warehoused data must be protected as well 

# Data Access Management/ SQL Services 
Traditionally, the database has been one of the main targets for attackers and malicious users. Syntaq utilizes the latest frameworks and methods to virtually neutralize programmatic issues (i.e. Entity Framework Core), and with regards to cloud deployment, it maximizes the protection through: 
- Enabling firewall rules for SQL Server 
- Enabling auditing on SQL Servers and monitoring the logs 
- Enabling object-level auditing on SQL Servers (Blobs) 
- Disabling SSH access on Network Security Groups from Internet 
- Disabling unrestricted TCP port 23 access (only authorized IPs) 
- SQL server threat detection is ‘On’ and set to ‘All’ 
- Setting email notification for anomalous activities on the database 
- Using Azure SQL Database transparent data encryption 

# Virtual Machines 
- Real-time endpoint protection for VMs 
- Latest OS patches for all virtual machines 
- Installation of VM agent to enable Azure Security Center for data collection 

Properly configuring Azure Security Center (ASC) with the abovementioned settings fulfils Syntaq’s role in the cloud provider/consumer dynamic as regards building up a secure system. The rest (such as network security, environmental security assurance, database patching, etc.) are guaranteed by Microsoft Azure cloud services as outlined by the provider in various readily available documents. 

# Incident Response Plan 
As part of the Business Continuity Plan (detailed in a separate accompanying document), Syntaq implements a thorough Incident Response Plan to cover contingencies on daily, monthly, half-yearly and annual bases. The plan lays out clear steps to be taken to avoid/deal with any occurrences that could in any shape or form hinder the continuous availability of the service. These include, but no limited to, security audits, monitoring, and overall maintenance of the entire system. 

Following is an overview of Syntaq’s IRP practices. For the detailed plan of action refer to Syntaq Incident Response Plan v1.0.0 document 
## IRP – ongoing: 
- Staff enabled and equipped to respond to a system breach 24/7 
- Regular security awareness training and programs for the admins 
- System configs reviewed and updated  
- Latest patches and best practices applied as soon as they emerge 
- New vulnerabilities addressed as soon as they emerge 
- System backup maintained  

## IRP – Daily: 
- Operational security procedures met 
- Log files, alerts, and events checked 
- New security risks identified and reported 

## IRP – Monthly: 
- Review critical security patches and system updates flagged by service providers 
- Review staff’s security performance and address concerns 

## IRP- Half-Yearly: 
Remove stored data outside the scope of business requirements 
Changing passwords across all domains 
Review of network security (routers, firewalls, etc.) 
Disable and remove inactive user accounts 
Perform internal and external vulnerability tests 

## IRP – Yearly: 
- Revamp cryptography keys 
- Review public web applications and APIs 
- Review development environment  
- Perform internal and external penetration test on app and network level 
- Review and update security policies 
- Update training material provided to employees 
- Maintain lists of business-critical system architecture 
- Test the Incident Response and Disaster Recovery plans 

## IRP - Major Events
The IRP also calls for a number of actions to be taken after each major change or event in the system. These include: 
- Conducting in-depth analysis of the system 
- Updating the flow diagrams 
- Updating system architecture  
- Reviewing web applications 
- Reviewing information security policies 
- Reliably documenting and storing information on roles and responsibilities 

# Disaster Recovery Plan
Operating as a SaaS (Software as a Service) puts Syntaq in an ideal position to respond to, and recover from, a disaster. With the application and the databases hosted on Microsoft Azure cloud, which provides its own safeguards with regards to disaster recovery, Syntaq clients can be sure that their data remains accessible and protected in any situation. This extends to the application service thanks to the measures observed by Syntaq as part of the Business Continuity Plan as well as the following practices: 
- Storing application documentation/wiki on cloud as well as locally to ensure quick and reliable access at all times 
- Preparing a comprehensive onboarding guide to get new agents up to speed on the workings of the application (development and production) in the shortest possible time 
- Training and empowering employees in terms of system knowledge to compensate for loss of leadership 
- Ensuring that IT and business staff are in full sync on the recovery plan 
- Regularly reviewing BC/DR documents to reflect all changes 
- Testing plans and recovery practice training 

For the detailed Disaster Recovery plan of action refer to document Syntaq Disaster Recovery Plan v1.0.0. 
