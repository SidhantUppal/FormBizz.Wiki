This section describes the operating considerations, issues, risks and impacts of our design.

# Availability and Reliability
The following are the availability and reliability considerations for this solution: 
|Consideration	| Rationale |Comments / Additional information|
|---|---|---|
Database Geo Replication |Provides Realtime fail over for continuity |Duplicates DB costs for each replicated node.|
|Redis Cache| Provide seamless continuation for User Session information during maintenance or restarting of the system	| Additional cost and not implemented|

# Capacity
The following are the capacity considerations for this solution: 
|Consideration	| Rationale |Comments / Additional information|
|---|---|---|
|Azure SQL Database Growth| Database should provide capacity for growth| Azure SQL Server provide for significant capacity required by large Enterprise storage and DTU needs|
|Archiving and records management|||

# Continuity
The following are the continuity considerations for this solution: 
|Consideration	| Rationale |Comments / Additional information|
|---|---|---|
|Web App Auto backups||Provided by Azure service infrastructure. Requires Standard or Premium service|
|SQL Server Auto Backups||Provided by Azure service infrastructure. Requires Standard or Premium service|

# Deployment / Implementation
|Consideration	| Rationale |Comments / Additional information|
|---|---|---|
|Web App plans that support deployment slots| Promote changes to staging slots for verification prior to go Live||
|Integration with CD Dev Ops pipeline from vendor| Automated deployment of approved artefacts from the vendors deployment pipeline||

# Performance
|Consideration	| Rationale |Comments / Additional information|
|---|---|---|
|Document Assembly Engine isolation| This process is run as a separate service from the main web app to avoid blocking the main web application resources. These resources can then be capacity manged separately. |The document assembly engine is the compute intensive part of the application.|
|Azure Web App environment that provides Scale up options| As production usage increases resources can be scaled up without re-deployment or downtime||

# Scalability
|Consideration	| Rationale |Comments / Additional information|
|---|---|---|
|Web App plans that support auto scaling| Auto scale as required| Can be configured based on Web App thresholds based on production usage|
|Azure App Service Environment (ASE)|If the App Service Environment can be deployed to an isolated environment where better control of compute resources, isolation, and network access can be provided||
|Azure Web App environment that provides Scale out options| Scale out options within the existing web app can be provided if an isolated App Service Environment is not required.||

# Systems Managements, Monitoring and Administration
|Consideration	| Rationale |Comments / Additional information|
|---|---|---|
|Privileged account management||Azure Active Directory (Azure AD) Privileged Identity Management (PIM) is a service that enables you to manage, control, and monitor access to important resources in your organisation.|
|Metrics and monitoring| Monitor and identify performance or capacity issues before they impact the operations of the system| Azure has comprehensive support for metrics on the Web App, Document Function and SQL Data base components. |
