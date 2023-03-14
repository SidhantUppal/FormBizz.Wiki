**Scribe Cypress Test Sample**

https://scribehow.com/shared/Azure_Workflow__vI2uFvmmR7SHvzslRJUNYg

**Install Cypress**
-	Install node, npm
https://nodejs.org/en/download/
-	Install cypress
npm install cypress –save-dev
-	Open cypress app and run test manually
.\node_modules\.bin\cypress open
-	Problem :“ps1 is not digitally signed. The script will not execute on the system”
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

**Run Cypress:**
In the cypres.json:
-define base text url: 
"baseUrl": "https://syntaq-falcon-test.azurewebsites.net",
-initialise the “username” and” password” under “env” key in order to log in the web
run cypress test
node_modules\\.bin\\cypress run

open cypress dashboard commands: npm run open
or: npm run test

please delete the record key when you run cypess test in local environment:
in the package.json file:
delete :"--record --key 891f388a-dbc7-4e6a-acfb-40cfc49c0080" under script

**Add/Edit Cypress test environment**

File of each branch: package.json

![image.png](/.attachments/image-055b6464-3ae9-4b36-b8fe-43b8bea6ad75.png)

**Debug Cypress**

_Problem1:_
-	Type in timeout issue
Situation: After default timeout expired, just type in half of the string rather than whole string in the automatic testing. Therefore, when tests try to find the component with whole expected string name, assertion failed.

Solution:  extend time out time to type command.
 ![image.png](/.attachments/image-d63bf73f-252d-4de6-9fc3-056109276b9b.png)


_Problem 2:_
-	cypress success locally but failed on CI server

Situation: 
Sometimes the test fails - not usually locally, it almost always fails on our continuous integration server. This maybe caused by the delay of our flaky tests when the application is running on our CI server.

Two Delay are main cause of this:
- The page is not fully retendered and loaded after get http response. 
- Animation is not finish.

Solution:

Find which element is change, and make assertion on whether that element is on finish status or not. The retry ability of Cypress will let the test retry unit timeout time expire. When changed element assertion pass, it means the page is loaded or updated successfully.

(take the code debug on the from page as example:)

-	Debug1:
Log in the system. Wait receive network response, and update page. Add assertion on a changed element to justify and wait the page is fully load and then do other command.
 
Before: 
![image.png](/.attachments/image-8fc76938-a256-4e66-895c-93d1d3b85cf4.png)
 
Fix and work code:
 ![image.png](/.attachments/image-e60c9d20-d42b-4fa7-93fa-55b2162b8aee.png)

- Debug2:
Wait animation finish. Create Modal pop up.

Before:
![image.png](/.attachments/image-dfe6c599-a379-461f-a8f6-a3bca4fae088.png)
 
After: the first added assertion wait the create from Modal load, the second added assertion wait Modal disappear.

![image.png](/.attachments/image-21065004-6f5b-493b-a065-bfddfd40d87f.png)

- Debug3: Delete Modal pop up and disappear

delete Modal:  Wait delete Modal append in the html dom.
Before:
![image.png](/.attachments/image-bec2507e-dd67-43aa-a465-5228da2ceb31.png)
After:
![image.png](/.attachments/image-e863da23-c740-4397-8951-77f34d1bd56e.png)

-  Debug 4
 After Create from, receive http response to refresh the from table. Write the assertion on the length of table change to wait from table updated. 
Before:
![image.png](/.attachments/image-2265fb11-daf1-41e0-be20-c0c9cca141b3.png)
After:
![image.png](/.attachments/image-13cd354e-e2e0-42c4-a0a7-c70a24454c13.png)

- Debug 5
Wait ACL share Modal load and finish
before
![image.png](/.attachments/image-03bfbe83-2b7c-49d9-a645-d6c7e63df37f.png)
after
![image.png](/.attachments/image-8133fad5-7b59-4f70-96d5-8c5b996e8f75.png)
- reference document: _`Retry-ability | Cypress Documentation`_

Other page such as document, record, voucher use the same theory. All the animation, and update of html page changes need the proper assertion to justify the changing element finish change, and then the following command can be success.

Problem3: Loading network 

Sometimes, it hard to find html element to make assertion whether html request finish and the page is updated. Therefore, we can use make assertion on get html response 200OK then we go to the next command. 

Before:
![image.png](/.attachments/image-119e64ff-513e-4124-a0d1-971362cc2bc4.png)
After:
![image.png](/.attachments/image-4e723118-a57e-4286-b833-7adbbda850d3.png)

Problem4: Form selection
When too many forms in the page, the new form cannot be selected or click, because it on the top and out of page. Therefore, during test, we need to make sure it is test in a brand new environment.
 ![image.png](/.attachments/image-979c0ae0-35bd-49b8-8083-00b44bada93b.png)

-	During test

Record and from should better be empty.

In the submission, it must has least one submission.

Problem 5: Azure running slower than local

Situation: Some command cannot finish within 4000ms, therefore, I extend the defaut timeout time into 6000ms.

Solution: Extend the timeout time in azure
 ![image.png](/.attachments/image-a1a1c2bb-0698-42d8-b03d-7e4d102325a6.png)

Problem6: 
1.	Test folder:
cypress\integration\5_Forms_Page\form_drag_drop.spec.js
scenario:
There are two errors:
Create a form, search form, exist, create a folder, search folder meet error.

Solution to Solve:
Add cy.get("#RefreshFormsButton").click() ;
Solved by changed the cypress test: refresh the page after search, then the data table can load new information when search.


**Integrate into Azure pipeline**
-	Before integration, Set up JUnit reporter on Cypress project
In package.json
 ![image.png](/.attachments/image-c6c8cfdd-0f74-4660-bf90-73b16ebcc65b.png)
In cypress.json
 ![image.png](/.attachments/image-6e591de7-03bb-4410-b897-37ae07400735.png)
-	Write Yml the Azure:




