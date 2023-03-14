Audit of data an how it is used and stored
Data processing activities
Client data & their clients data

3rd party services we use - Sendgrid, GA

Need to look at getting our team up to speed with data security
IASME
ISO27001
Cyber Essentials

Online form fill
Where info is held, how it is processed + what happens if the user wants access, update or delete the data
Ability to fully download the data held by the company
Need to even consider data in back ups - IP address and log files
Details of all cookies on teh platform , how to access and change + links to contact the DPO
Data subject rights = right to be forgotten!!!

Privacy Policy
Data protection and security policy
Risk committee
Staff updates and education
Board 
Privacy by design principal

Relevant Articles - 
https://blog.pcisecuritystandards.org/are-you-ready-for-30-june-2018-sayin-goodbye-to-ssl-early-tls
https://www.eugdpr.org/
https://kinsta.com/blog/gdpr-compliance/

Key Features
Features
•	Consent management
•	Privacy Preference management for Cookies with front-end preference UI & banner notifications
•	Privacy Policy page configurations with version control and re-consent management
•	Rights to erasure & deletion of website data with a double opt-in confirmation email
•	Re-assignment of user data on erasure requests & pseudonymization of user website data
•	Data Processor settings and publishing of contact information
•	Right to access data by admin dashboard with email look up and export
•	Right to access data by Data Subject with front-end requests button & double opt-in confirmation email
•	Right to portability & export of data by Admin or Data Subject in XML or JSON formats
•	Encrypted audit logs for the lifetime of Data Subject compliance activity
•	Data Subject Secret Token for two-factor decryption and recovery of data
•	Data breach notification logs and batch email notifications to Data Subjects
•	Telemetry Tracker for visualizing plugins and website data

Settings
General
From the Settings options in the dashboard, you can select the Privacy Policy page for tracking and logging consent.
On login, the user must consent to the Privacy Policy outlined on the site. If the user does not consent, the user will not be registered or logged in.
If the site owner updates the Privacy Policy page content, the change will be logged and flagged to the admin that they must notify users on next login to seek re-consent. Additionally, the warning message can be dismissed in the event of a minor correction or mistake.
Additionally, under General Settings the Admin can set the outgoing email limitation which would set the batch notification email limit per hour in the event of a Breach Notification.
Cookie Preference Management
Similar to consent management, users can opt in or out of cookies that are being used on the site. There are 3 formats of cookies that can be created which include:
•	Always Active: Cookies that are always active or are required for the site to function.
•	Toggled: Cookies that can be activated or blocked based on the user preference
•	Opt-Out Link: Cookies that require configuration from a third-party source in order to opt-out
Depending on the user preference setting, you can use the is_allowed_cookie( $cookie ) function to save and set the cookies. The cookie with the user approved cookies can be found at another cookie named gdpr_approved_cookies. There’s also a helper function called is_allowed_cookie( $cookie ) that you can use to prevent setting up a cookie.
Consent Management
Consents can be registered on the settings page. They can be optional or not. By default, this plugin comes with a Privacy Policy consent that users need to agree with on registration.
For optional consents, there’s a wrapper function have_consent( $consent_id ) to help you display or hide something on the site depending if the user gave consent or not.
Consents are logged to the user record for auditing or for access purposes.
Requests Table & Rights of Data Subject
Right to Erasure Requests
•	The Data Subject is able to submit a request to be erased from the site using a shortcode.
•	When a request is made, the Data Subject will receive an email confirmation to confirm the deletion request.
•	After email confirmation, the user request is added to the requests table for review by the Administrator. The Administrator can also add a user manually with an email look up and review.
•	If the Data Subject has content published on the site for any post types or comments, they will be added to this table. If they do not have any content, they will receive a confirmation of erasure request and be provided a 6 digit Token for safekeeping after erasure in case of recover data needs.
•	The requests table allows the Administrator to reassign any content to another user or delete it.
•	In the event of comments, the Data Subject’s content would be made anonymous.
•	Admin can also manually add users to the erasure requests table with a manual email search
Right to Access Data Request & User Data Portability
•	The Data Subject can place a request to download their data with the shortcode.
•	After requesting their data, the user will receive a double opt-in confirmation email then the plugin will generate an XML or JSON file, which will be emailed to them for download with an expiration time of 48 hours.
Right to Rectify & Complaint Requests
•	The Data Subject can place a request to rectify data or file a complaint with the shortcode.
•	After making their request, the user will receive a double opt-in confirmation email and then add them to the table for admin to handle the request.

Tools
Access Data
The Access Data tool allows the Admin to look up a user email and view the data of a particular user. The Admin can download and export the data in a JSON or XML format and provide to the Data Subject if manually requested.
NOTE: This method should not be used without the Data Subject confirming their identity.

Audit Log
Everything the Data Subject does from registration, providing consent to the privacy policy, terms of service and other requests are logged and encrypted in a database. Data breach notifications are also logged to all Data Subjects upon confirmation by Controller.
•	Using the Data Subject’s email, you can look up and retrieve the user information and display it.
•	If the Data Subject has been removed from the site, this encrypted log is deleted from the database and saved as an encrypted file inside the plugin folder.
If in the future, the Data Subject makes a complaint or there is a need to recover the data, the user can provide their email address and the 6 digit token they received from the deletion confirmation email to decrypt and retrieve the file.

Data Breach & Notifications
In case of a data breach, the Admin can generate a Data Breach Notification to users by logging the information and confirm the breach through a double opt-in confirmation email. The following information would be recorded in the audit log:
•	Nature of the personal data breach
•	Name and contact details of the data protection officer
•	Likely consequences of the personal data breach
•	Measures were taken or proposed to be taken
Once the confirmation of the breach has been confirmed via email, the website will begin a batch email notification process to all users every hour until all users receive the notification.

Telemetry Tracker
The Telemetry Tracker feature will display all data that is being sent outside of your server to another destination. It will indicate the plugin or theme responsible, file and line where the data is being sent.
WordPress Core and some plugins gather data from your install and send this data to an outside server.
WordPress Plugin Repository does not allow plugins to do that, but premium plugins are able to do this because they are not bound by the Plugin repository rules. If you did not explicitly opt-in for this feature you should make a complaint.
Important!

Activating this plugin does not guarantee that an organization is successfully meeting its responsibilities and obligations of GDPR. Individual organizations should assess their unique responsibilities and ensure extra measures are taken to meet any obligations required by law and based on a data protection impact assessment (DPIA).




