This section provides a high-level view of the security architecture, describing the architectural goals, constraints and assumptions for this solution design, including any design decisions and architectural risks raised or discovered during the project. 

# Overview 
The following is the security architecture from a broad conceptual perspective.  

Included is a high-level discussion on the following areas and how they might be impacted or changed for this solution, or whether they are new: 

- user management,  
- authentication (user and application), 
- data and information services. 

# Security architecture goals 

The following security architecture goals have been considered for this solution: 

The Syntaq platform is a multi-tenanted Sass application based on the application boilerplate and ASPNET Zero framework. This framework aims to provide solutions to common Sass and enterprise application concerns. 

- https://aspnetboilerplate.com/Pages/Documents/Introduction  
- https://docs.aspnetzero.com/en/aspnet-core-mvc/latest/ 

|Goal |Comments |
|---|---|
|Isolation of Tenancy Data using Repository level filters |Some tenancy isolation controls have be turned off. This was in response to RFP requirements on sharing of data, forms and templates between tenancies. |
|Application of Policies that apply authorisation checking for users against Access Control lists (ACL’s) stored in the system. |These ACL’s provide access to data (Entities) created by users in the system. Records, RecordMatters, RecordMatterItems, Forms and Templates. Levels: Owner, View, Edit |
|Role based access to application functions.| Role based access to application functions are configurable. AS such there is no ‘standard’ list of which functions are accessible by a role. These roles and functions are only configurable by a Host or Tenant administrator.|
|Editions | Configurable edition features which can be applied to tenants (agencies) |
|Automatic Cross Site Forgery Protection | System has recently been updated to .net 3.1 from .net core 2.1. This new version has been deployed to the MBIE test/pilot (but not production site). CSFR has not been validated for this version yet. CSFR tokens are baked into the framework for requests and validation. |
|User and Tenant impersonation ||
|Two Factor Authentication (Email, SMS, Google Authenticator) |
|User Lockout ||
|OpenId Connect Authentication ||
|Log and show all login attempts for users ||
|Password complexity settings | |

## Security architecture constraints 
The following security architecture constraints have been identified for this solution: 
|Constraint |Comments |
|---|---|
|Tenancy Isolation |Some tenancy isolation controls have be turned off for MBIE. This was in response to RFP requirements on sharing of data, forms and templates between tenancies ||

## Regulations and Standards
The solution has to comply with the following regulation and standards: 
|Constraint |Comments |
|---|---|
|||

## Privacy and Confidentiality
The solution needs to address the following privacy and/or confidentiality concerns.
|Constraint |Comments |
|---|---|
|||

# Security Controls
We have implemented the following security controls
|Control name| Description| Comments|
|---|---|---|
||||

# Identity and Access Management
## Security User Roles
The following security user roles have been identified for this solution:  
|User | Description | Comments / additional information |
|---|---|---|
||||

# Authentication
## Access Rules
The following security user roles have been identified for this solution:  
|Rule| Description | Comments / additional information |
|---|---|---|
||||
 



