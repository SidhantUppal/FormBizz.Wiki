#Link GitHub commits, pull requests, and issues to work items

##Purpose 

The purpose of linking work items with develop branch is automatically update the status of work items and generate release note.

##Methods
There are three ways of link work items
* when commit code, in the commit comment add “AB#BranchID”， for example:"fixed AB#8062"

When release, if branch 8062 is merged in this build. This work item will pop up in the release note.

The following picture shows the how the commit comment change the status of work items and how to link the work items with commit message: 
![image.png](/.attachments/image-c2db9d29-6b1f-4f5f-ad86-ca070d8a2fbb.png)
reference: https://docs.microsoft.com/en-us/azure/devops/boards/github/link-to-from-github?view=azure-devops&viewFallbackFrom=azure-devops%22%20%5Cl%20%22%3A~%3Atext%3DLinking%20to%20a%20GitHub%20issue,choose%20Add%20Link%3EExisting%20item

* pull request
When create a new pull request, you can link the workitems in the Description using "#BranchId"
![image.png](/.attachments/image-9ff82505-948e-4e14-b420-d6f550c15d07.png)
reference: https://docs.microsoft.com/en-us/azure/devops/notifications/add-links-to-work-items?view=azure-devops

 or select work items to link
![image.png](/.attachments/image-88933cc4-9fcc-4320-87be-96a6e80a725e.png)



* Using Azure devops cards directly:
click add link to link the completed branch with work items
![image.png](/.attachments/image-d78811d4-3b0c-47cb-bd18-fef000dc0a1f.png)

* After we linked branch and work items we can generate release note with associated work items in the wiki:
![image.png](/.attachments/image-b2440af2-b953-4be8-a435-976ac35d543e.png)

