# Overview
Outlines the Hardware and Software Specifications for a Developer.

## Prerequisites 
1. Install Visual Studio, minimum version 15.4.4. Recommended Edition is Professional or Enterprise. When installing, make sure you include the Mobile development with .NET using Xamarin option.

1. Install MS SQL Server & MS SQL Server Management Studio.

1. Run & connect MS SQL Server Management Studio to your local DB instance.

1. In the left-hand navigation bar, underneath the server instance, right click on the Databases folder and select New Database. 

1. Enter the database name FalconDb. 

1. Download Node.js & follow the installation wizard through.   [https://nodejs.org/en/download/]()

1. Download Yarn & follow the installation wizard through.  [https://yarnpkg.com/lang/en/docs/install/#windows-stable]()

1. To install Gulp, open up a new command prompt window and run "npm install gulp@next -g"

1. Before opening the solution open a command prompt in the root directory of *.Web.Mvc project and run "yarn" command to install client-side dependencies.
Before running the project, we need to run a npm task to bundle and minify the CSS and JavaScript files. In order to do that, we can open a command prompt, navigate to root directory of *.Web.Mvc project and run npm run create-bundles command. This command should be run when a new npm package is being added to the solution

1. Run Visual Studio, then //How to connect to Team Server

1. Download a copy of Syntaq.Falcon from Team Services/Server?

1.  Load the project, then go Tools > NuGet Package Manager > Package Manager Console. This will open the Package Manager Console at the bottom of the window.

1. Make sure Default Project is set to Syntaq.Falcon.EntityFrameworkCore at the top of the Package Manager Console.

1. Inside the console, type "Add-Migration", then when prompted, supply the name of the database (FalconDb). 

1. Next type in the console window "Update-Database". This will generate a local copy of the latest database structure.








