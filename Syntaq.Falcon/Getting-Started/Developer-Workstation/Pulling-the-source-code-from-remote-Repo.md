
If you need to pull the latest version of the source code from the remote repository and you already have the database deployed on your workstation, you will need to change the Connection Strings before you can run the program. 

Open Web.Mvc solution > open appsettings.json
Under "ConnectionStrings" comment out the string for the production environment and un-comment the string for "localhost"

You won't have to re-execute migrations, but it is still a good idea to run an Update-Database before building and running the application.

** If you don't have an instance of the DB on your machine, follow the steps mentioned in the [Development Environment Setup](https://zumesoft.visualstudio.com/Syntaq/_wiki/wikis/Syntaq.Falcon.wiki/18/Development-Environment-Setup-List) guide to create and populate the database.
I