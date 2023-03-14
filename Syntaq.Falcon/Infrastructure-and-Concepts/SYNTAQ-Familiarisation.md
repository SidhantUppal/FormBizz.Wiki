# Syntaq Familiarisation
 
- IMPT Authorisation checking . Syntaq uses  the ACL manager to authorise access to entities in the system. Any public methods accessing an entity needs to perform this check where it is not excclusivley controlled by roles permission checking. View the Syntaq source code and see where this has been applied. This is not part of the ASPNETZERO framework

if (_ACLManager.CheckAccess(new ACLCheckDto() { Action = "Edit", ………………

- IMPT Role Checking. Public methods access is also controlled by role checking which is configured by the edition features set. This role checking is applied on the public controller methods using a Filter (see below)

[AbpAuthorize(AppPermissions.Pages_Forms_Create, AppPermissions.Pages_Forms_Edit)]
                                  
- Familiarise with the Syntaq API Swagger UI (syntaq-falcon-test.azurewebsites.net)
- ACLs
- AppJobs
- Apps
- Folders
- FormFeedbacks
- FormRules
- Forms
- Projects
- RecordmatterContributors
- Records
- Recordmatters
- Recordmatteritems
- Submissions

# Exercises
1.	Create a call in PostMan Download Postman | Try Postman for Free to create a new Form via the API
2.	Configure the Form submission workflow to create a document
3.	Trigger the Form to Run via the API (configure submission form workflow first in the form builder)

# SYNTAQ Assembly Familiarisation
