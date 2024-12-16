### SharePoint File Upload Service

## Service Route
`/spfileintegration/import/sharepointfileintegration`

## Description
The SharePoint File Upload service is triggered via a webhook at a specific point in the workflow and uploads one or more files to a SharePoint folder using the REST API. The destination folder for the files is specified in the `sharepointFolder` template variable. If the variable is not sent to the integration service, the file(s) will be uploaded to the Documents folder.

If a non-existing folder is provided in the `sharepointFolder` variable, the service will automatically create the required folder hierarchy and upload the file(s) to the specified folder.

This service supports both **on-premise** SharePoint and **Office 365** SharePoint environments. It is compatible with the respective authentication methods for each platform, including **NTLM authentication** for on-premise instances and **token-based authentication** for Office 365.

For more details on how the SharePoint API works, visit [Working with Folders and Files with REST](https://learn.microsoft.com/en-us/sharepoint/dev/sp-add-ins/working-with-folders-and-files-with-rest).

## Dedicated Template Variable

- **sharepointFolder**: Specifies the SharePoint folder where files will be uploaded. If not given, the file(s) will be uploaded to the Documents folder by default. If a non-existing folder is specified, all necessary folders will be created automatically.

---

This service is part of the Itiner Workspace integrations and facilitates seamless file transfer to Microsoft SharePoint.
