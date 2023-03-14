Security, and especially data security is very much at the forefront of our design principles. We understand that the data we collect on behalf of our clients is sensitive and valuable.
 

# User Access 
SYNTAQ portals have a complete authorization system with rich login options. 
- We provide our administrators with User and Role management pages, 
- Hierarchical organizational units system (Teams) to group users and entities.  
- User login, registration, password reset- and email validation, 
- User, roles and permission based authorization, 
- Two factor authentication (Email, Google Authenticator), 
- User lockout,
- Log and show all login attempts for users,
- Password complexity settings, 
- Automatic Cross-Site Request Forgery protection, 

# Authentication 
Authentication and then authorisation of access to data is checked in depth at every level of the application. 

The system employs a domain driven model approach. This approach enforces the validation of models at each level of the application to ensure well-formed and complete requests or posts. However, the unstructured user defined form schemas do not enforce these rules and are open by intention. 

Tenant administrators have to decide how they want their users to be authenticated  
- Standard username and password login 
- Two factor authentication, which is an optional setting 
- Integration with Identity Server4 which allows us to take advantage of Microsoft single sign on for custom integration clients 

# Encryption 
All data that passes between you and SYNTAQ’s web application is encrypted using industry-standard protocols.  

Data is transparently encrypted on site to ensure the database cannot be removed from site. Personally, identifiable data is masked to all users except from administrators and authorised users. 

Admin access to all our assets is restricted via IP, these expire on a regular basis. 

**TBC – check with Bruce if we have applied the at rest masking…** 

# Availability 
SYNTAQ’s web applications are hosted, maintained and delivered via extremely secure and reliable Microsoft Azure Cloud Services.  
SYNTAQ has implemented hosted Disaster Recovery services provided by Microsoft Azure for; 
- Our application servers and Database servers, which has a 90-day point-in-time restore, and 
- User files (Forms and Document Templates) recovery services for up to 90-days point-in-time restore. 

# Backups 
SYNTAQ operates a point-in-time restore back-up facility. This allows us, should there be any corruption, to restore a historical version of the entire database from a point within the previous 90-days period.  

# Security Audits 
Syntaq is based on the ASP.NET Boilerplate framework as referenced on https://www.owasp.org/index.php/OWASP_ASP.NET_MVC_Boilerplate_Project. Our development process include review for the OWASP Top 10 list.    
 
The core application framework used by SYNTAQ falcon has been scanned for vulnerabilities with the latest version of OWASP ZAP (v2.7.0). The OWASP Zed Attack Proxy (ZAP) is one of the world's most popular security tools and is actively maintained by hundreds of international volunteers. 

All the positive alerts reported by the automated scanner have been fixed. The remaining alerts were able to be stated as false-positive.   