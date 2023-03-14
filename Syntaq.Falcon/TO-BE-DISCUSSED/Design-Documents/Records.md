## Entities

/****** Object:  Table [dbo].[SfaRecord]    Script Date: 26/06/2018 4:28:13 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[SfaRecord](
	[Id] [uniqueidentifier] NOT NULL,
	[UserId] [Bigint] NOT NULL,
	[OrgId] [bigint] NOT NULL,
	[Name] [varchar](255) NULL,
	[Description] [varchar](2048) NULL,
	--[DateCreated] [datetime] NULL,
	[RecordFolderID] [uniqueidentifier] NULL,
	[FormData] [varchar](max) NULL,
 CONSTRAINT [PK_AssemblyNotifictions] PRIMARY KEY NONCLUSTERED 
(
	[ID] ASC
)WITH (STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY] TEXTIMAGE_ON [PRIMARY]
GO

ALTER TABLE [dbo].[SfaRecord] ADD  CONSTRAINT [DF_AssemblyNotifictions_ID]  DEFAULT (newid()) FOR [Id]
GO

ALTER TABLE [dbo].[SfaRecord] ADD  CONSTRAINT [DF_AssemblyNotifictions_Date]  DEFAULT (getutcdate()) FOR [DateCreated]
GO

/****** Object:  Table [dbo].[SfaRecordMatter]    Script Date: 26/06/2018 4:18:12 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[SfaRecordMatter](
	[Id] [uniqueidentifier] NOT NULL,
	[UserID] [bigint] NOT NULL,
	[OrgId] [bigint] NOT NULL,
	[FormFolderId] [bigint] NULL,		-- folderid of the craetign form
	[FormId] [uniqueidentifier] NULL, -- id of the creating form
	--[DateCreated] [datetime] NULL, -- AUTOGENERATED?
	--[DateUpdated] [datetime] NULL, -- AUTOGENERATED?
	[RecordFolderID] [uniqueidentifier] NULL, -- ? Include
	[Data] nvarchar(MAX) NULL, -- saved data from form
	[SessionID] [varchar](50) NULL,
 CONSTRAINT [PK_UsersInfoFile] PRIMARY KEY NONCLUSTERED 
(
	[ID] ASC
)WITH (STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY] TEXTIMAGE_ON [PRIMARY]
GO

ALTER TABLE [dbo].[SfaRecordMatter] ADD  CONSTRAINT [DF_SfaRecordMatter_ID]  DEFAULT (newid()) FOR [ID]
GO

ALTER TABLE [dbo].[SfaRecordMatter] ADD  CONSTRAINT [DF_SfaRecordMatter_Date]  DEFAULT (getutcdate()) FOR [DateCreated]
GO

ALTER TABLE [dbo].[SfaRecordMatter] ADD  CONSTRAINT [DF_SfaRecordMatter_DateUpdated]  DEFAULT (getutcdate()) FOR [DateUpdated]
GO

/****** Object:  Table [dbo].[SfaRecordMatterItem]    Script Date: 26/06/2018 4:28:13 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[SfaRecordMatterItem](
	[Id] [uniqueidentifier] NOT NULL,
	[UserId] [Bigint] NOT NULL,
	[RecordId] [uniqueidentifier] NULL,
	[RecordMatterId] [uniqueidentifier] NULL,
	--[DateCreated] [datetime] NULL,
	[DocumentName] [nvarchar](255) NULL,
	[Document] [image] NULL,
	[FormId] [uniqueidentifier] NULL,
	[FormData] [varchar](max) NULL,
	[SystemFee] [money] NULL,
	[UserFee] [money] NULL,
	[ReviewerFee] [money] NULL,
	[DocID] [int] IDENTITY(15000,1) NOT NULL,
	[FormURL] [nvarchar](2048) NULL, -- ?? Application derived
	[AllowWord] [bit] NULL,
	[AllowWordPaid] [bit] NULL,
	[AllowPDF] [bit] NULL,
	[Assembled] [bit] NULL
 CONSTRAINT [PK_AssemblyNotifictions] PRIMARY KEY NONCLUSTERED 
(
	[ID] ASC
)WITH (STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY] TEXTIMAGE_ON [PRIMARY]
GO

ALTER TABLE [dbo].[SfaRecordMatterItem] ADD  CONSTRAINT [DF_AssemblyNotifictions_ID]  DEFAULT (newid()) FOR [ID]
GO

ALTER TABLE [dbo].[SfaRecordMatterItem] ADD  CONSTRAINT [DF_AssemblyNotifictions_Date]  DEFAULT (getutcdate()) FOR [DateCreated]
GO
GO

ALTER TABLE [dbo].[SfaRecordMatterItem] ADD  CONSTRAINT [DF_SfaRecordMatterItem_AllowWord]  DEFAULT ((0)) FOR [AllowWord]
GO

ALTER TABLE [dbo].[SfaRecordMatterItem] ADD  CONSTRAINT [DF_SfaRecordMatterItem_AllowWordPaid]  DEFAULT ((0)) FOR [AllowWordPaid]
GO

ALTER TABLE [dbo].[SfaRecordMatterItem] ADD  CONSTRAINT [DF_SfaRecordMatterItem_AllowPDF]  DEFAULT ((1)) FOR [AllowPDF]
GO

ALTER TABLE [dbo].[SfaRecordMatterItem] ADD  CONSTRAINT [DF_SfaRecordMatterItem_Assembled]  DEFAULT ((0)) FOR [Assembled]
GO

/****** Object:  Table [dbo].[UsersInfoFileFolder]    Script Date: 26/06/2018 4:40:45 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[SfaRecordFolder](
	[Id] [uniqueidentifier] NOT NULL,
	[ParentID] [uniqueidentifier] NULL,
	[Name] [varchar](50) NULL,
	[Description] [varchar](255) NULL,
	[DisplayOrder] [smallint] NULL,
 CONSTRAINT [PK_SfaRecordFolder] PRIMARY KEY CLUSTERED 
(
	[ID] ASC
)WITH (STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY]
GO

ALTER TABLE [dbo].[SfaRecordFolder] ADD  CONSTRAINT [DF_SfaRecordFolder_ID]  DEFAULT (newid()) FOR [ID]
GO

