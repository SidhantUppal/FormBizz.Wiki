##Setting Up External Resources
There are certain database actions that require access to external resources, like a Reporting database, that gets its data from one or more Production databases. 
####Creating a Master Key and Scoped Credential
Before we can create external resources, we need to create a scoped credential and a master key to protect the scoped credential. 

`CREATE MASTER KEY ENCRYPTION BY PASSWORD = 'p@ssw0rd';`

The code above creates a master key, secured by the specified password. Ask your supervisor about which password you should use. 

`CREATE DATABASE SCOPED CREDENTIAL ZumeForms_AU_Cred WITH IDENTITY = 'ZFAdmin', SECRET = '???????';`

The code above creates a scoped credential, which is an authentication record for connecting to an external resource. For example, if our resource is a database, then identity is a database users username, and the secret is a password for that user account. Ask your supervisor about which credentials to use.

####Creating an External Database & External Table Reference

Once we have a set of credentials, we can now create our external resource references.

`CREATE EXTERNAL DATA SOURCE ZumeForms_AU WITH`
`(`
    `TYPE = RDBMS,`
   ` LOCATION = 'zumesoft-au-se.database.windows.net,1433',`
    `DATABASE_NAME = 'ZumeForms_AU' ,`
    `CREDENTIAL = ZumeForms_AU_Cred`
`)`

The code above creates an external database reference, and in the case of the example above, this is creating a reference the Australian production server. Name the reference appropriately and ask your supervisor about which location string and database name to use. 

An external database reference is required in order to make an external table reference or in order to use an external stored procedure.

`CREATE EXTERNAL TABLE [dbo].[Users](`
	`[DateCreated] [datetime] NOT NULL,`
	`[IDMVC] [int] NOT NULL,`
	`[UserName] [varchar](255) NULL,`
	`[AddressCountry] [nvarchar](50) NULL`
`)`
`WITH`
`(`
	`DATA_SOURCE =  ZumeForms_AU`
`);`

The code above creates an external table reference, and in the case of the example above, this is creating a reference to the Users table on the Australian production server. Only the columns you intend to access need to be specified in the reference, ask your supervisor for the column type definitions, as the reference columns need to match the source columns. Make sure to specify the correct data source where the table is located.

You can alias table names by including an alias after the table name on the first line.

## Accessing External Resources

Once your database and table references have been set up,  you can make use of them. When using a referenced table, you can simply refer to it as if it were a local table, either by its name or if you used an alias, by that alias. 

`EXEC sp_execute_remote N'ZumeForms_Reporting',...`

When running an external stored procedure, you reference the external database reference as the first parameter, as seen above, so that the sp_execute_remote function knows where it can find the stored procedure. 