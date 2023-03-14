This section provides an overview of the data, database is deployed and managed in terms of the architecture, sources and ownership, logical model and considerations for persistence, retention and privacy of the data.  

# Overview
Designing object-oriented software is hard, and designing reusable object-oriented software is even harder, but just keeping the focus on reusability is not enough. In order to deliver the desired quality to the end user, an application must also exhibit a wide variety of architectural requirements:

Usability, which is concerned with characteristics such as aesthetics and
consistency in the user interface.
- Reliability, which is concerned with characteristics such as availability, accuracy
of system calculations, and the system’s ability to recover from failure.
- Performance, which is concerned with characteristics such as throughput, response
time, recovery time, start-up time, and shutdown time.
- Supportability, which is concerned with characteristics such as testability,
adaptability, maintainability, compatibility, configurability, installability,
scalability, and localizability.

In order to meet all these demands the design of the architecture of an application becomes an important and vital task in a software development cycle. 

## Logical Data Model
Diagrams show only primary tables focusing on the Tenant/User and main entities created by the system.

### Tenant/ user Logical Data Model
![tenant user data model.png](/.attachments/tenant%20user%20data%20model-b92db35d-8a68-4751-9220-10fc27e77246.png)
![tenant user data model 2.png](/.attachments/tenant%20user%20data%20model%202-de68cd4b-ac78-49fb-87e0-892d5cf6a993.png)

## Data Classification
|Entity/Repository/System |Classification| Description/ Consequences|
|---|---|---|
|abpAuditLog / SQL | Unclassified / In-confidence / Sensitive / Restricted / Confidential / Secret / Top Secret |Contains public API request data|
|abpUsers / SQL |Confidential|	Personably identifiable information such as names, addresses and other contact information |
|sfaRecordMatter, sfaRecordMatterItem / SQL| Unclassified / In-confidence / Sensitive / Restricted / Confidential| Data collected from users through Forms and App submissions. From personally identifiable information, confidential information and sensitive information. Including the completed document output from the system|

## Data Replication

## Data Storage, Archiving and Retention

## Data migration

## Records Management





