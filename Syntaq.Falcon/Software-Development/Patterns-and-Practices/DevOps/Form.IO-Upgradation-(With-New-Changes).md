 **Analysis**
1. Current version on 9145 branch of the library --4.15.0-rc.13".
2. The different versions required to work are:
- Npm version required -- 6.14.6
- Node version required -- 10.22.1
- Gulp version required :

         --  [ CLI version -- 2.3.0 ] 
         --  [ Local version -- 4.0.2] 

![image.png](/.attachments/image-975ebad8-d228-4bcc-b6cf-27b77819e639.png)

**Problems while Installing the required versions**:
**Step 1.** To install Npm specific version :

    -- npm install -g npm@#required_version.

**Step 2.** To install Node specific version :

    -- Download specific version.
    -- Uninstall the version installed into the sytem.
    -- Install the version required after downloading.

**Step 3.** To install Gulp specific version :

    -- For global use with slush: [ CLI version -- 2.3.0 ] 
         npm install --save gulp-install

    -- For local use with gulp : [ Local version -- 4.0.2] 
         npm install --save-dev gulp-install
****
**_Still facing issue while installing the gulp Local version:_**

- **_[ Searched Issue : ReferenceError: primordials is not defined ]_** 

1. Either add npm-shrinkwrap.json file in the same directory where the package.json is added with the defined functionality as below:

![image.png](/.attachments/image-e128e563-e055-499e-8b07-ce3068ac4b8b.png)

     Run the command in command prompt as :

   **npm install**

After installation, the reflection will be like this:

![image.png](/.attachments/image-fdccfd24-6abc-42e4-bdd5-6dce653d58b6.png)


2. **Local version** in reflected as **Unknown**

     -- Rerun the gulp installation, it will automatically install the version required in the project.

3. **Webpack relevant issue :**

     -- run the command: "npm install"

How to run project :

**Step 1 :** Execute the command "Build gulp" : 

In command prompt :

![image.png](/.attachments/image-1544b877-b643-48df-9ac6-6006aab3234f.png)

**Incase, Webpack error occured :**

Run command **"npm install"**, it will resolve the issue. 

**Step 2 :** Run the project.

## Added new Components as replacement of Base component than the prior versions as follows:

         - Field
         - Input
         - MultiValue

- **Directory structure:**

Base classes are stored in the "components/_classes" folder.
- Field
- Input - All input element derive from this class.
- MultiValue - Handles multiple valued components
- Nested - Handles all nested components.

    ![image.png](/.attachments/image-b5c79741-a92d-4b68-9714-4985839d8c11.png)

# **Merge**
1. **The steps to merge each form.IO component:** 
- Add our customer components in Index.js and builder.js under component file
- Add our customer component in Builder.js under Form.IO file
- go to the *.form.js file and change the super class
- (Change from Base component to relative new core components in the latest version)
- go to related *.edit.data, *.edit.display, *.edit.validation merge our customer properties.
- go to *.js to get, set the value of this component, change the constructor, and render function if needed 
- run save and submit, wizard page change to see whether the data flow through correctly or not
- run component release check related to this customer component.

2. Need to rewrite some functions in x.js file

**Some functions needed to be rewrite:**
- Use getClass() function to add our customer "systaq-component" class
- rewrite createElement() to render() or ejs template

![image.png](/.attachments/image-a0c122e6-d936-4eaf-9433-88521e152675.png)

- addEventListenser move to Attach() function
- Using ref to find related component, some times need to rewrite getValue(), setValue(),setValueAt(),updateValue()

**Steps to integrate a new FormIO component:**

- Add component into the Index.js, builder.js under component file hierarchy.
- Builder.js under FormIO file to add component, use component.form.js()
- check the display.edit.form file to modify the new function of formio component.


       Builder.js file under "Components" directory

![image.png](/.attachments/image-d96a262a-7671-4274-8a94-3e4e95590d2b.png)


       Index.js file under "Components" directory

![image.png](/.attachments/image-86777822-7c69-4411-af82-0a97d5475186.png)



In upgraded version, the basic rendering schema is changed.  

**Previously we imported :** 

import BaseComponent from '../base/Base';

![image.png](/.attachments/image-7ea8f0e2-135a-4aa2-afda-6b3611df33a3.png)

**In upgraded version,** we use libraries defined under formIo/src/components/_classes/* as follows into the custom components as, some examples are: 

- import Input from '../_classes/input/Input';
- import Field from '../_classes/field/Field';
- import Component from '../_classes/component/Component';
- import Nested from '../_classes/nested/NestedComponent';

![image.png](/.attachments/image-49160c54-659c-498c-a694-250f92f65650.png)


**Or the components defined under components as predefined components as follows:** 

- import Button from '../button/Button';
- import File from '../file/File';

![image.png](/.attachments/image-612018f2-c5a1-4c76-b081-8df55f8473e3.png)

**Render Process of components:**

![image.png](/.attachments/image-1a77605f-579e-4387-8367-1b4272c43196.png)


## **The difference between buildcomponent:**

- Old version: 

![image.png](/.attachments/image-40e189cf-eff7-481b-ba44-4f4bb75e94e4.png)

- Current version : 

![image.png](/.attachments/image-88cf6108-48e4-4d89-8794-b712895375e6.png)

## Different function to render component:

- Old version:

![image.png](/.attachments/image-7dfbca6f-0809-4eff-b1fa-be906565645b.png)

- Current version :

![image.png](/.attachments/image-7ce9ccb6-be09-4b1a-9b58-8662e111809f.png)

## How to write customer css

### old version how to add customer css

![image.png](/.attachments/image-fb5de46d-6c32-427d-bd99-99fd11847617.png)

###  New version, for example in the label.js

![image.png](/.attachments/image-1d44a3f8-1fba-471f-a3bb-a2b2bf861049.png)









