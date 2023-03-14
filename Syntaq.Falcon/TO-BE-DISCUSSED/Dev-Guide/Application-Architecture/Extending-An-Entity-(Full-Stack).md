## Extending User Functionality (Full Stack)
![LayersToProjects(ExtendUser).png](.attachments/LayersToProjects(ExtendUser)-b1a45960-cf15-4b1e-a383-68032adce9aa.png =550x500)
Before you get started, remember to check out the latest version of the project. 
1. Start by extending Falcon.Core/Authentication/Users/User.cs
1. In the Package Manager Console (PMC), with EntityFrameworkCore selected in the default project dropdown, run the command "Add-Migration". When prompted, enter in a name for the migration.
1. While still in the console, run an "Update-Database" command. 
1. If extending the admin's user management interface, extend Falcon.ApplicationShared/Authorisation/Users/DTO/UserEditDTO.cs & UserListDTO.cs. If extending a users profile interface, extend Falcon.ApplicationShared/Authorisation/Users/Profile/DTO/CurrentUserProfileEditDTO.cs
1. If extending the admin's user management interface, extend Falcon.Mvc/Areas/Falcon/Views/Users/CreateOrEditModal.cshtml. If extending a users profile interface, extend Falcon.Mvc/Areas/Falcon/Views/Profile/MySettingsModal.cshtml
1. For any new label names you've created, extend Falcon.Core/Localization/Falcon/Falcon.xml. To see changes applied, rebuild and restart the application.
1. Go to the tests project, extend and run unit tests (list unit tests)
1. If the unit tests succeed, commit the code changes to the repository. 