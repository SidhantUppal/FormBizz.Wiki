# Notes for build
**Build Number**:1809   
**Total Work Items Resolved** :51

#  New Features
        *  **8867**  Feedback form Export table
        *  **8858**  Syntaq.js changes for ALportal-In host and Test branch
        *  **8062**  Create a Table to store changes made to a Template/ Form/ Project Template-Track Frequency 
        *  **8795**  Add the upload file function to Projects Tab and Documents
        *  **8529**  Projects - When logging back into a form you are always taken back to the start. Can we take the user back to the page where they saved and exited?
        *  **8805**  ProjectTemplateIDs to be added to form data-IS144
        *  **8794**  Projects UI Updates
        *  **8735**  UI - Update to the projects UI and workflow
        *  **8452**  Project “description” on the project details view does not appear to be editable via the UI 
        *  **8732**  Build CI pipeline
        *  **8570**  As a Tenant Admin that is sharing a Project or form with another tenant, I want the ability to know which templates have been shared using an icon, so that I dont have to click into each template to see if it has been shared or not
        *  **8703**  As a User starting a new project, I want to be redirected to the &quot;Project Details&quot; page so that I dont have to select a Project

#  Bug fixes
        *  **8886**  IS-165 JSON export converts special characters
        *  **8880**  IS-174 NZBN general search issues -Also IS158
        *  **8846**  Duplication of generated files when file names change IS-125
        *  **8843**  MBIE - Feedback 13082021
        *  **8835**  LC and IS-159 -address group issues
        *  **8585**  Dashboard Add admin permission to 4 widget.
        *  **8845**  Switching tabs in rules builder can create large white space in the Builder Tab
        *  **8848**  IS-155 Rules import don&#x27;t replace old rules with the same name
        *  **8754**  Date Control - Display in Timezone will not set to UTC
        *  **8860**  Modification of Frequency type of change
        *  **8859**  UI - Shadow around form page breadcrumbs in Test environment
        *  **8812**  IS 012 Consideration: the Left hand navigation (crumbs) are too deep causing scrolling issues
        *  **8849**  IS-160 Submit button not working in SIT consistently
        *  **8721**  Cannot set the placeholder value property of a text field using the logic section of the field. Field remains unchanged
        *  **8780**  Save script notification is blank
        *  **8838**  MBIE-Upload file not work in the hidden form component
        *  **8823**  IS152-Ability to retrieve a full list of all steps and their current statuses within a project
        *  **8832**  LC-Summary inconsistencies-Also problem formMBIE
        *  **8829**  Fix deploy issuse 09082021
        *  **8785**  Saving an empty or invalid rule should not be allowed - causes UI issues
        *  **8821**  05082021_deploy bug fixes
        *  **8363**  Width slider doesn&#x27;t work for Nested Form Component
        *  **8816**  Click Final unlock back to draft status
        *  **8790**  Jump back to project tab
        *  **8803**  IS 051 Assign an index to repeated items
        *  **8813**  IS145 important flag display trigger
        *  **8810**  IS143 Checkbox groups mandatory flag no longer working
        *  **8804**  IS 060 Prompt to ask form builder if they want to keep their unsaved changes
        *  **8793**  Deployment: v8.8.0.0 [20210719] Bug fixing
        *  **8789**  IS-136 Saving an empty HTML tag will prevent the form from loading
        *  **8782**  Show upload File next to the generated documents
        *  **8781**  Cannot re-search the  NZBN search term
        *  **8604**  Click on page with no required fields contributor modal is presented but if I run the same process but with a page with a required field I get the error message 
        *  **8611**  Form UI - Clear repeat issues
        *  **8733**  Section CSS styling has dropped out
        *  **8291**  window not scaling down on data table elements
        *  **8496**  Datatable issue out of line again
        *  **8679**  Merge issue caused customer dashboards disappear 2020 years ago comes again


#  Associated commit comments
        * Message: WIP   Commited by: brucefallen
        * Message: MERGE   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8880-IS-174-NZBN-general-search-issues&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8846-Run-Record-through-App&#x27; into Master-Test   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8881-Project-Search-not-working&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8754-Date-Control-Display-in-Timezone-not-set-to-UTC&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8835-LC-IS-159-address-group-issues&#x27; into Master-Test   Commited by: brucefallen
        * Message: MERGE   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8867-Feedback-form-Export-table&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8886-IS-165-JSON-export-converts-special-characters&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge branch &#x27;Master-Test&#x27; of https://zumesoft.visualstudio.com/Syntaq/_git/Syntaq.Falcon into Master-Test   Commited by: brucefallen
        * Message: 8863 Tenant Sharing Approval
8630 Tenant Sharing Dynamic values in Workflow
8875 Word Docs downloading as PDF
8862 Apply ACL Checks to Project Templates   Commited by: brucefallen
        * Message: Updated _CreateOrEditModal.js typo   Commited by: John Jiang
        * Message: IS-165 JSON export converts special characters AB#8886   Commited by: Tong Yu
        * Message: AB#8880   Commited by: Tong Yu
        * Message: AB#8880   Commited by: Tong Yu
        * Message: Updated project button ID in project &gt; Index.js and .min.js   Commited by: John Jiang
        * Message: AB#8846   Commited by: Tong Yu
        * Message: change Tag &gt; Action button style   Commited by: John Jiang
        * Message: Remove comment codes   Commited by: John Jiang
        * Message: Fixed the bug cannot-read-property-aocolumns-of-undefined.   Commited by: John Jiang
        * Message: UI of Tag and Value consolidation   Commited by: John Jiang
        * Message: Update azure-pipelines.yml for Azure Pipelines- change the wiki builder method, don&#x27;t allow generate duplicate card info   Commited by: Tong Yu
        * Message: Main functions of tag and tag value consolidated done. UI polishiing yet to work on   Commited by: John Jiang
        * Message: AB#8843   Commited by: Tong Yu
        * Message: Merge   Commited by: brucefallen
        * Message: AB#8867   Commited by: Tong Yu
        * Message: AB#8835   Commited by: Tong Yu
        * Message: Update Users &gt;Excel Export Operations button style to be consistent with others   Commited by: John Jiang
        * Message: Update getAll fiter   Commited by: John Jiang
        * Message: Merge   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8860-Modification-of-Frequency-type-of-change&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8848-NEW-IS-155-Rules-import-replace&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8845-Switching-tabs-in-rules-builder-can-create-large-white-space-in-Builder-Tab&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8843-MBIE-Feedback-13082021-Second&#x27; into Master-Test   Commited by: brucefallen
        * Message: Step Audit History updates   Commited by: brucefallen
        * Message: AB#8843 fixed the log name of project   Commited by: Tong Yu
        * Message: Dashboard Add admin permission to 4 widget. AB#8585   Commited by: Tong Yu
        * Message: Add admin permission  to 4 Dashboard widget. AB#8585   Commited by: Tong Yu
        * Message: AB#8845   Commited by: Tong Yu
        * Message: AB#8848   Commited by: Tong Yu
        * Message: Render the tag value table in Tagvalue _CreateOrEditModal.js. Next step is to apply the tagid filter in the table   Commited by: John Jiang
        * Message: test   Commited by: John Jiang
        * Message: add get values of a tag   Commited by: John Jiang
        * Message: logs   Commited by: John Jiang
        * Message: AB#8754   Commited by: Tong Yu
        * Message: AB#8860   Commited by: Tong Yu
        * Message: AB#8860   Commited by: Tong Yu
        * Message: Fixed Assembly by URL or ID   Commited by: brucefallen
        * Message: some changes   Commited by: John Jiang
        * Message: Merge remote-tracking branch &#x27;origin/8848-IS155-Rules-import-replace-old-rules-with-same-name&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8859-UI-Shadow-around-form-page-breadcrumbs&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: AB#8859   Commited by: Tong Yu
        * Message: fixed UI Shadow around form page breadcrumbs AB#8859   Commited by: Tong Yu
        * Message: Update New/Export Project Template buttons style   Commited by: John Jiang
        * Message: Merge   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: edit value 1 to 1   Commited by: John Jiang
        * Message: AB#8858 master test branch   Commited by: Tong Yu
        * Message: AB#8858   Commited by: Tong Yu
        * Message: AB#8062   Commited by: Tong Yu
        * Message: AB#8062   Commited by: Tong Yu
        * Message: fixed IS-155 Rules import don&#x27;t replace old rules with the same name AB#8848   Commited by: Tong Yu
        * Message: Merge remote-tracking branch &#x27;origin/8721-logic-section-cannot-set-placeholder-for-text-feilds&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8780-Save-script-notification-is-blank&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8849-IS-160-Submit-button-not-working-consistently&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: 8857 Tenant Assembly Engine Email   Commited by: brucefallen
        * Message: 8857 Tenant Assembly Engine Email   Commited by: brucefallen
        * Message: Embeded Repeat Document Assembly File Format Fix   Commited by: brucefallen
        * Message: 1. Added clear button beside search buttons in all navigation Bars;
2. Standardised all search buttons&#x27; UI.   Commited by: John Jiang
        * Message: 8828-Validation-removed-from-number-fields-on-row-add   Commited by: brucefallen
        * Message: 1. Standardise First letter capitalisation;
2. Export To Excel button style consitency.   Commited by: John Jiang
        * Message: Tenat Variables Update   Commited by: brucefallen
        * Message: 1. Changed Projects &gt; search project button ID to be same as in the host;
2. Fixed Doc Templates &gt; search template button;
3. Fixed Form &gt; search form button;   Commited by: John Jiang
        * Message: fixed AB#8812   Commited by: Tong Yu
        * Message: AB#8849   Commited by: Tong Yu
        * Message: AB#8721   Commited by: Tong Yu
        * Message: AB#8721   Commited by: Tong Yu
        * Message: fixed AB#8780   Commited by: Tong Yu
        * Message: 8808-IS-139 ListFormat mergefield is adding unwanted extra spaces   Commited by: brucefallen
        * Message: 8772-IS-137 Custom data source, and logic blocks evaluate in build form view   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: Fixed Host Timeconvert null   Commited by: brucefallen
        * Message: Merge branch &#x27;Master-Test&#x27; of https://zumesoft.visualstudio.com/Syntaq/_git/Syntaq.Falcon into Master-Test   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: fixed issuse1 and anon css issuse   Commited by: Tong Yu
        * Message: Merge   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: Merge branch &#x27;Master-Test&#x27; of https://zumesoft.visualstudio.com/Syntaq/_git/Syntaq.Falcon into Master-Test   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: Merge branch &#x27;Master-Test&#x27; of https://zumesoft.visualstudio.com/Syntaq/_git/Syntaq.Falcon into Master-Test   Commited by: Tong Yu
        * Message: fixed issuse1, and issuse3   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: fixed AB#8838   Commited by: Tong Yu
        * Message: Merge remote-tracking branch &#x27;origin/8785-Saving-an-empty-or-invalid-rule-should-not-be-allowed&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8832-Summary-Inconsistency&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8784-Colours-non-standard-for-rules-builder-actions&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Update azure-pipelines.yml for Azure Pipelines- change filter of generate release note   Commited by: Tong Yu
        * Message: C157 Project Step / Inheritance
C117 Project Audit Date
Trigger project Template seach by Checkbox click
Security Remediate fixes. Password History, Default Admin user name   Commited by: brucefallen
        * Message: fixed feedback bugs from MBIE AB#8843   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: fixed bug AB#8823   Commited by: Tong Yu
        * Message: fixed Colours non-standard for rules builder actions AB# 8784   Commited by: Tong Yu
        * Message: Fixed Embeded Session expiry issue   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: fixed LC-issues summary table inconsistency AB#8832   Commited by: Tong Yu
        * Message: Merge remote-tracking branch &#x27;origin/delete-8812&#x27; into Master-Test   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: Tong Yu
        * Message: undo 8812   Commited by: Tong Yu
        * Message: Fixed ExportProjectDocument function   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8829-Fix-deploy-issuse-09082021&#x27; into Master-Test   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: AB#8829   Commited by: Tong Yu
        * Message: fixed Saving an empty or invalid rule should not be allowed - causes UI issues AB#8785   Commited by: Tong Yu
        * Message: Merge   Commited by: brucefallen
        * Message: Modified ProjectTemplateId functionality   Commited by: brucefallen
        * Message: AB#8821   Commited by: Tong Yu
        * Message: Fixed ProjectStartLayout   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8363-Width-slider-doesn&#x27;t-work-for-Nested-Form-Component&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8813-IS145-important-flag-display-trigger&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8803-repeatpanel-index-json-object&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge branch &#x27;Master-Test&#x27; of https://zumesoft.visualstudio.com/Syntaq/_git/Syntaq.Falcon into Master-Test   Commited by: brucefallen
        * Message: generate release note when the branch has&#x27;Master&#x27; tag   Commited by: Tong Yu
        * Message: Merge   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8816-Click-Final-unlock-back-to-draft-status&#x27; into Master-Test   Commited by: brucefallen
        * Message: fixed bug AB#8363   Commited by: Tong Yu
        * Message: Merge remote-tracking branch &#x27;origin/8812-IS-012-navigation-crumbs-causing-scrolling-issues&#x27; into Master-Test   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: fixed IS-012 the Left hand navigation are too deep causing scrolling issues. AB# 8812   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: AB#8816 click final back to draft status   Commited by: Tong Yu
        * Message: finished AB#8062   Commited by: Tong Yu
        * Message: WIP   Commited by: Tong Yu
        * Message: 8795-change the way to generate rmi in project   Commited by: Tong Yu
        * Message: AB#8790 finish   Commited by: Tong Yu
        * Message: AB#8790 WIP   Commited by: Tong Yu
        * Message: 8803- fixed AB#8803   Commited by: Tong Yu
        * Message: 8803-Wip   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: Tong Yu
        * Message: fixed bug IS145 important flag display trigger AB#8813   Commited by: Tong Yu
        * Message: finished   Commited by: Tong Yu
        * Message: Merge remote-tracking branch &#x27;origin/deployment-Bug-fixes-3-4&#x27; into Master-Test   Commited by: brucefallen
        * Message: Finished add features add upload files to project tab AB#8795   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: fixed AB#8529   Commited by: Tong Yu
        * Message: WIP   Commited by: Tong Yu
        * Message: Merge   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8789-IS-136-Saving-an-empty-HTML-tag-will-prevent-the-form-from-loading&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8803-IS051-Assign-an-index-to-repeated-items&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8804-Prompt-to-ask-form-builder-keep-unsaved-changes&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8810-IS143Checkbox-groups-mandatory-flag-no-longer-working&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8805-ProjectTemplateIDs-to-be-added-to-form-data&#x27; into Master-Test   Commited by: brucefallen
        * Message: fixed Bug ProjectTemplateIDs to be added to form data-IS144 AB#8805   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: fixed Checkbox groups mandatory flag no longer working AB#8810   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: Fixed Bug form builder unsaved prompt AB#8804   Commited by: Tong Yu
        * Message: Merge remote-tracking branch &#x27;origin/8793-DeploymentBugFixing&#x27; into 8046-Document-Version-History   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: uncomment send email AB#8794   Commited by: Tong Yu
        * Message: WIP   Commited by: Tong Yu
        * Message: fixed Bug Assign an index to repeated items AB#8803   Commited by: Tong Yu
        * Message: AB#8794   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: fixed bugs AB#8793   Commited by: Tong Yu
        * Message: Initial Commit   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: Merge branch &#x27;Master&#x27; of https://zumesoft.visualstudio.com/Syntaq/_git/Syntaq.Falcon into Master   Commited by: brucefallen
        * Message: 8791 - Emailing user an unauthenticated link to a record shows an error   Commited by: brucefallen
        * Message: Fixed GetForm for anon users via token   Commited by: brucefallen
        * Message: Project Start Fixes   Commited by: brucefallen
        * Message: fixed BUG IS-136 Saving an empty HTML tag will prevent the form from loading AB#8789   Commited by: Tong Yu
        * Message: Update azure-pipelines.yml for Azure Pipelines   Commited by: Tong Yu
        * Message: Merged   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8782-Show-upload-File-next-to-generated-documents&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8781-Cannot-Re-search-search-term&#x27; into Master-Test   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8452-Project-Editable&#x27; into Master-Test   Commited by: brucefallen
        * Message: fixed project not store upload file problem AB#8782   Commited by: Tong Yu
        * Message: allow download all recordmatteritems   Commited by: Tong Yu
        * Message: uncomment &quot;hasSteps&quot; function   Commited by: Tong Yu
        * Message: Merge branch &#x27;8735-Merge&#x27; of https://zumesoft.visualstudio.com/Syntaq/_git/Syntaq.Falcon into 8735-Merge   Commited by: Tong Yu
        * Message: AB#8735   Commited by: Tong Yu
        * Message: Merge branch &#x27;8735-UI-Update-projects-UI-and-workflow&#x27; into 8735-Merge   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: fixed AB#8781   Commited by: Tong Yu
        * Message: fixed Bug NZBN cannot research   Commited by: Tong Yu
        * Message: WIP AB#8782   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: Fixed ParentId on folder   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: added migration script for achrive column   Commited by: Tong Yu
        * Message: Merged   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: finished change ui of project AB#8735   Commited by: Tong Yu
        * Message: Fixed : FileUpload, Embedded Styles, Form Icons   Commited by: brucefallen
        * Message: Feedback Form Fixes   Commited by: brucefallen
        * Message: MB BUG196, MB BUG197, MB BUG193, MB BUG163, MB BUG178, MB BUG199   Commited by: brucefallen
        * Message: MBIE Branch Merged   Commited by: brucefallen
        * Message: Merge From MBIE Branch   Commited by: brucefallen
        * Message: Removed STQ_PRODUCTION compile switch on MergeTextsAppService   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: Fixed Embedded Logo Uploads   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: ui changes #8735   Commited by: Tong Yu
        * Message: Added registration Logger statements   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: change all project page   Commited by: Tong Yu
        * Message: changed start new project modal   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: Removed STQ_PRODUCTION compile falg   Commited by: brucefallen
        * Message: Modified DocumentTemplate &quot;LockToTenant&#x3D;true&quot; as default   Commited by: brucefallen
        * Message: Security Pen Test 2.0   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: Merged SAML integration
Welcome Email Falcon references removed   Commited by: brucefallen
        * Message: added new feature edit project modal AB#8452   Commited by: Tong Yu
        * Message: Merge   Commited by: brucefallen
        * Message: Merge branch &#x27;Master-8.8&#x27; of https://zumesoft.visualstudio.com/Syntaq/_git/Syntaq.Falcon into Master-8.8   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Update azure-pipelines.yml for Azure Pipelines   Commited by: Tong Yu
        * Message: Build CI pipeline AB#8732   Commited by: Tong Yu
        * Message: Build CI pipeline AB#8732   Commited by: Tong Yu
        * Message: Build CI pipeline AB#8732   Commited by: Tong Yu
        * Message: Added Zeren publish file   Commited by: brucefallen
        * Message: Cleaned Publish Profiles   Commited by: brucefallen
        * Message: Start Project User/Author role fix   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: 8738 - All Projects are set to Final in production
Added Default Final Status for RecordMatters not part of a Project   Commited by: brucefallen
        * Message: Merged   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8604-no-required-fields-contributor-modal-pop-up-error&#x27; into Master-8.8   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8586-Project-template-search-not-work&#x27; into Master-8.8   Commited by: brucefallen
        * Message: Merge branch &#x27;Master-8.8&#x27; of https://zumesoft.visualstudio.com/Syntaq/_git/Syntaq.Falcon into Master-8.8   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: Update azure-pipelines.yml for Azure Pipelines   Commited by: Tong Yu
        * Message: need to integrate XUNIT test in master8.8   Commited by: Tong Yu
        * Message: added run test yaml file   Commited by: Tong Yu
        * Message: Update azure-pipelines.yml for Azure Pipelines   Commited by: Tong Yu
        * Message: made warning modal css style consitent AB#8604   Commited by: Tong Yu
        * Message: Fixed bug search button for project template not work AB#8686   Commited by: Tong Yu
        * Message: Added new features  icon showns when  templates have been shared AB#8570   Commited by: Tong Yu
        * Message: adding new features AB#8570   Commited by: Tong Yu
        * Message: fixed BUG Click on page with no required fields contributor modal is presented but if I run the same process but with a page with a required field I get the error message  AB#8604   Commited by: Tong Yu
        * Message: fixed 8673   Commited by: Tong Yu
        * Message: fixing formUI CSS style   Commited by: Tong Yu
        * Message: fixing AB#8611, #8733   Commited by: Tong Yu
        * Message: Merge   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8679-MB-Dashboard-Loading-Issue&#x27; into Master-8.8   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: Merge   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: fixed bug Data table css issue AB#8291 AB#8496   Commited by: Tong Yu
        * Message: fixed bug of tenant dashboard loading issue AB#8679   Commited by: Tong Yu
        * Message: Merge   Commited by: brucefallen
        * Message: Merge remote-tracking branch &#x27;origin/8529-MB-logging-back-form-back-to-the-saved-page&#x27; into Master-8.8   Commited by: brucefallen
        * Message: Fixed Jump to Project Details page, start project button disappear issuse. AB#8703   Commited by: Tong Yu
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: WIP   Commited by: brucefallen
        * Message: 8529 finish mb log back to saved page   Commited by: Tong Yu
        * Message: Unit test baseline all running   Commited by: brucefallen
        * Message: 8456-11-hasn&#x27;t passed left   Commited by: Tong Yu
        * Message: 8456-commit   Commited by: Tong Yu
        * Message: 8456-commit   Commited by: Tong Yu
        * Message: 8456-commit   Commited by: Tong Yu
        * Message: 8456-commitch-aloow add app   Commited by: Tong Yu
        * Message: Baseline running scripts   Commited by: brucefallen
        * Message: commit   Commited by: Tong Yu
