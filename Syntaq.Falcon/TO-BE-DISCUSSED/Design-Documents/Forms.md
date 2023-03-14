
/****** Object:  Table [dbo].[SfaForms]    Script Date: 26/06/2018 4:13:26 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[SfaForms](
	[Id] [bigint] IDENTITY(1,1) NOT NULL,
	[CreationTime] [datetime2](7) NOT NULL,
	[CreatorUserId] [bigint] NULL,
	[Description] [nvarchar](2048) NULL,
	[FormsFolderId] [bigint] NOT NULL,
	[RecordsFolderId] [bigint] NOT NULL,
	[RecordSaveToOwnerFolder] [bit] NOT NULL,
	[DocPDF] [bit] NOT NULL,
	[DocUserCanSave] [bit] NOT NULL,
	[DocWord] [bit] NOT NULL,
	[DocWordPaid] [bit] NOT NULL,
	[LastModificationTime] [datetime2](7) NULL,
	[LastModifierUserId] [bigint] NULL,
	[Name] [nvarchar](128) NULL,
	[PaymentAmount] [decimal](18, 2) NOT NULL,
	[PaymentCurr] [nvarchar](3) NULL,
	[PaymentEnabled] [bit] NOT NULL,
	[TenantId] [int] NULL,
 CONSTRAINT [PK_sfaForms] PRIMARY KEY CLUSTERED 
(
	[Id] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO


/****** Object:  Table [dbo].[SfaFormsFolder]    Script Date: 26/06/2018 4:39:26 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[SfaFormsFolder](
	[Id] [uniqueidentifier] NOT NULL,
	[ParentID] [uniqueidentifier] NULL,
	[Name] [varchar](50) NULL,
	[Description] [varchar](255) NULL,
	[System] [bit] NULL,
	[DisplayOrder] [smallint] NULL,
 CONSTRAINT [PK_Folders] PRIMARY KEY CLUSTERED 
(
	[ID] ASC
)WITH (STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY]
GO

ALTER TABLE [dbo].[SfaFormsFolder] ADD  CONSTRAINT [DF_Folders_ID]  DEFAULT (newid()) FOR [ID]
GO

ALTER TABLE [dbo].[SfaFormsFolder] ADD  CONSTRAINT [DF_SfaFormsFolder_System]  DEFAULT ((0)) FOR [System]
GO

ALTER TABLE [dbo].[SfaFormsFolder] ADD  CONSTRAINT [DF_SfaFormsFolder_Order]  DEFAULT ((1)) FOR [DisplayOrder]
GO

