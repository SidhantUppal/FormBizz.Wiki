**1. The Breaking changes for formio -3.13.2 to 4.15.0-rc.13(lastest):**
where to check formio version:
**\Syntaq.Falcon.Web.Mvc\wwwroot\assets\formio\package.json

- Previous formio component inherent from " BaseComponent from '../base/Base';"
In the lastest version formio component inherent from 
![image.png](/.attachments/image-e3a8e50e-53ac-43a8-b58c-1b45c2ca05e8.png)

-  use form templates(.ejs file) to render formio componennt as html
use ejs template(javascript to render html)
https://help.form.io/developers/form-templates
The image below shows the differences of build component between old version and new version
![image.png](/.attachments/image-46a3f8a6-ac1d-4dc1-8052-45db1cf7ae28.png)

The old version to create input element
![image.png](/.attachments/image-121992f7-007c-4850-a24f-263ea670f4b9.png)

The new version to create input element
![image.png](/.attachments/image-7b6aa395-96ec-4c17-9b25-4239809690c0.png)

Add customer template in formio:
E:\Syntaq.Falcon\src\Syntaq.Falcon.Web.Mvc\wwwroot\assets\formio\src\templates\bootstrap\index.js

- Change flag in the updateValue function(define component is changed or not)
old version: use getFlag function
newversion: delete this function

- New  formio.js library uses refs to refer to parts of the DOM. These can then be selected regardless of where they are in the DOM.
https://help.form.io/developers/form-templates#template-references-refs

**2. The steps to merge Formio:**
- Download lastest version of formio from Github

https://github.com/formio/formio.js

- To run formio:
Upgrade the node.js to lastest version
Yarn install
Yarn build
yarn add -D vanilla-text-mask
yarn build or gulp build

gulp -v
CLI version: 2.3.0
Local version: 4.0.2


**3. The steps to merge each formio component** 
- Add our customer components in Index.js and  builder.js under component file
- Add our customer component in Builder.js under formio file 
- go to the *.form.js file and change the super class 
(change from Base component to relative new core components in the lastest version)
- go to related *.edit.data, *.edit.display, *.edit.validation merge our customer properties
(Know the new feature and add our customer feature in it)
- go to *.js to get, set the value of this component, change the constructor, and render function if needed(see details in section 4)
- run save and submit to see whether data flow through correctly or not
- run component release check related to this customer component

**4. Need to rewrite function in x.js file** 

   Some functions needed to be rewrite:
- Use getClass() function to add our customer "systaq-component" class
 - rewrite createElement() to render()  
- rewrite creatInput() to renderTemplate()
- addEventListenser move to Attach() function
- rewrite getValue(),  setValue(),setValueAt(),updateValue()

 

