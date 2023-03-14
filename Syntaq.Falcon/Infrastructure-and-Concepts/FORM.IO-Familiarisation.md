Form.IO Familiarization
Available documents: 
1.	Below is the formio documentation:
https://help.form.io/developers/introduction
2.	This is the FormIO open-source code
https://github.com/formio/formio.js
3.	Our FormIO project under Syntaq project is located under 
E:\Syntaq.Falcon_New_Location\src\Syntaq.Falcon.Web.Mvc\wwwroot\assets\formio\
Use gulp build to loading formio project into Syntaq Portal

Familiarise the following functions of Form IO:
1.	There are several ways to load form
-	Loading directly form from 
https://syntaq.com/Falcon/forms/load
-	loading form from project
{https://syntaq.com/Falcon/forms/loadInProject}
	-       loading form from record
	-       loading form from anonymous user
	-       loading form from nested form
	-       loading form from pop up form
2.	Build Form 
E:\Syntaq.Falcon_New_Location\src\Syntaq.Falcon.Web.Mvc\wwwroot\assets\formio\Builder.js
3.	Embedded Form
4.	Adding ruler script and logic to control form component 
5.	Loading data when form is initialised
6.	Form save, submit in the syntaq.js

Exercises:
7.	Using Form schema and createForm function to create a form
8.	Using Formio.FormBuilder function to config build slider bar
9.	In the syntaq.js, set debugger at 'initialized', 'change', 'render', have a look on when they are called, and what kind of functions added in these event.
10.	Test ‘save’ and ‘submit ’ event in the syntaq.js and have a look what back-end functions are called
