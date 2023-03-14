# Creating a Service Principle

1. Log in to Azure Subscription
1. Search for, then go to, App Registrations 
1. Register a New App Registration, give it a name and pick an account type
1. In a new tab, go to the resource to what to grant access to the Service Principle too
1. In the resources Access Control (IAM) settings, Add a new Role Assignment
    1. Select an appropriate role
    1. Set access to Azure AD user, group or service principle
    1. In the select option, type in the name of the resource - when it appears, select it
    1. Save the role assignment
1. Go back to the previous tab where you have the app registration open
1. Click on the Certificates & Secrets setting, then create New Client Secret


# Connecting a Service Principle

1. Under Azure DevOps's Project Settings's Service Connections, Click New Service Connection
1. Select the Azure Resource Manager option
1. In the Modal that opens, click on the use the full version of the service connection dialogue link
1. Enter in a connection name, choose the AzureCloud environment option, and choose the appropriate scope level
1. Copy your subscription id and name from Azure and paste them into the matching fields
1. Copy the Service Principle Client Id from the Application (client) Id in your Registered App in Azure
1. Copy the Service Principle Key from the Client Secret Key you created earlier
1. Copy the Tenant Id from the Directory (client) Id in your Registered App in Azure
1. Verify the Connection - if it fails, troubleshoot, if it passes then save the Service Connection