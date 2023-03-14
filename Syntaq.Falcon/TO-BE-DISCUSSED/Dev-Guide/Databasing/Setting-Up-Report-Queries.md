##Before you get started
When developing SQL queries, it is always important to keep query efficiency and speed in mind, as you don't want a query slowing down or locking up database resources. 

When you are developing reporting queries, particularly cross-database queries, the speed and efficiency of the query is even more important. Consider the example below:

![ElasticQueryLayouts.png](.attachments/ElasticQueryLayouts-cc2b3489-7065-49cd-8b37-dc20d49325cb.png)

In the first scenario, we have a logic app that runs a SQL script on the reporting database, which then requests data from one or more production databases, awaits a response and then processes the returned data. 

This method ends up producing a lot of round trips, with each request and response encountering network latency, which ultimately slows down the process, holding resources for longer and generally being a slow query method.

The second and third scenarios, by contrast, work far more efficiently. In each scenario, the workflow is triggered on the production database, either by a trigger, a timed stored procedure or by a logic app. The first action is responsible for collecting the data from the production database, before sending each result set to the reporting database for processing there. By keeping the processing on the servers, and by only making one-way network transmissions, the overall speed and efficiency of the processes are increased, resulting in faster queries. 

## Report Query via Trigger
Setting up a trigger is straightforward and easy, simply:
1. Log into SQL Server Mangement Studio.
1. Remember to check with your supervisor first, but connect to the desired SQL Server.
1. Expand the Databases folder, then expand the desired production database icon.
1. Expand the Tables folder, then expand the table icon of the table you want the trigger to run from.
1. Right-click on the Triggers folder and select New Trigger from the context menu.
1. Mangement Studio will generate a trigger template for you in the editor window, which will look like this:
![Capture.PNG](.attachments/Capture-7635e3b4-4290-46d5-926b-795569f072fe.PNG)
1. You can remove the if exists logic, and then customize the remainder of the template by giving the trigger a name, specifying a target table and what action will initiate the trigger, as indicated below:
![Capture.PNG](.attachments/Capture-69dcf7ac-90e3-42f3-b488-14eaf2928103.PNG)
1. All the remains now is to add the query to the trigger and save.

**Tip:** The name of the trigger should start with "TR_" as this is the naming convention for denoting that an item is a trigger. 

## Report Query via Stored Procedure
Setting up a trigger is straightforward and easy, simply:
1. Log into SQL Server Mangement Studio.
1. Remember to check with your supervisor first, but connect to the desired SQL Server.
1. Expand the Databases folder, then expand the desired production database icon.
1. Expand the Programmability folder, then right-click on the Stored Procedures folder, hover on New and then select Stored Procedure from the context menu.
1. Mangement Studio will generate a Stored Procedure template for you in the editor window, which will look like this:
![Capture.PNG](.attachments/Capture-678fc7b7-4f49-4375-9013-a09476ba0634.PNG)
1. You can now customize the template, giving the stored procedure a name, specify parameters, if any, that the procedure should get in or pass out, and fill in the author, date and description comment, like so:
![Capture.PNG](.attachments/Capture-2690c4e2-fb58-47a2-b734-e5dd8989eb13.PNG)
1. All the remains now is to add the query to the stored procedure and save.

**Tip:** The name of the stored procedure should start with "usp_" as this is the naming convention for denoting that an item is a user stored procedure.

####Calling a remote stored procedure
For creating reporting queries, you will also need to call stored procedures on remote servers. Luckily this is also relatively straightforward. A remote stored procedure call is made up of five parts; an executive call to run a remote procedure, a external resource, the procedure name and parameter placeholders, the parameter types, and the parameters and values. For example:

`EXEC sp_execute_remote N'ZumeForms_Reporting',` <- The executive call and external resource name
`N'[dbo].[usp_ExampleTask] @Domain, @TenantId, @TenantName',` <- The procedure name and parameter placeholders
`N'@Domain nvarchar(128), @TenantId int, @TenantName nvarchar(128)',` <- The parameter types
`@Domain = 'create.zumesoft.com.au',` <- A parameter and value
`@TenantId = @LTenantID,` <- A parameter and value
`@TenantName = @LTenantName` <- A parameter and value