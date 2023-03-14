![NetZeroGitMerging.jpg](/.attachments/NetZeroGitMerging-1ff7c323-046f-4435-849a-48cb40e0694d.jpg =350x600)
## Part 1: Updating Framework-Master
1. Log into aspnetzero.com
1. Go to aspnetzero.com/download
   - Download the latest version of .Net Zero with the following settings:
   - Project Name = Syntaq.Falcon
   - Protect Type = AS<span>P.N</span>ET CORE MVC & jQuery
   - Project Version = Latest Stable
   - Application Area Name = Falcon
1. Open the existing project and switch to the Framework-Master branch.
1. Open the existing project in File Explorer after the branch as switched over and delete all but the following files:
   - .git Folder
   - .gitignore
   - tsconfig.json
1. Open the new project and copy its files into the now empty current project folder. Don't override the kept files.
1. Run data base migrations if required. Package manager, EntityFramework core - update-databse
1. Commit the changes to the local repository and sync to the remote repository.

**NOTE:** ON First run you may login may return Json output. 
**Fix:** open a powershell prompt in the root directory of *.Web.Mvc project and run "yarn" command to install client-side dependencies.


**NOTE:** ON First run you have style sheet and js libraries missing. Run "npm update" 
**Fix:** open a powershell prompt in the root directory of *.Web.Mvc project and run "npm update" command to install client-side dependencies.

**NOTE**: Task Runner Explorer contains the list of automated functions .Net Zero uses gulp to run tasks. These taks need to be successful before application can run

**NOTE**: npm run create-bundles to bundle and minify css and js
 
1. Commit changes to Frame-work master branch

## Part 2: Creating Merge-Branch
~~1. Switch to the Master Branch and once the branch has switched over, make a copy of the files locally.~~
1. Create a new branch from the Framework-Master branch called Merge-Branch-X, where X is the new version number. This new branch will automatically receive a copy of the code from Framework-Master.
1. Switch to the new branch and run a merge from Master into Merge-Branch-X.
1. Resolve any merge conflicts that are encountered.
      1. STQ Added Files Select 'Stage' These are our Entity Files
1. Update any out-of-date NuGet packages.
1. In File Explorer, navigate to the root of the MVC project, open a CMD or Powershell window and run the command 'yarn' in the MVC root folder, followed by 'npm run create-bundles'.
1. Compile and Run the project. Troubleshoot any conflicts encountered.
1. Check that all previous functionality is still functioning and that all Unit Tests pass. 
1. Commit changes to the local repository and sync to the remote repository.

## Part 3: Updating Master
1. Switch to the Master branch and run a merge from Merge-Branch-X into Master.
1. Compile and Run the project.  Troubleshoot any conflicts encountered.
1. Commit changes to the local repository and sync to the remote repository. Keep Merge-Branch-X until the next update.
