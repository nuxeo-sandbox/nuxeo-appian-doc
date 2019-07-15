# Nuxeo Appian Application Integrations

The Appian integrations invoke a collection of Nuxeo REST endpoints.  Many of the endpoints can be used as blueprints to build against other [Nuxeo REST](https://doc.nuxeo.com/nxdoc/rest-api/) endpoints.  Nuxeo provides an [API Playground](https://nuxeo.github.io/api-playground/) to build additional integrations for the Appian server.

## Integration: NX_AuthenticationToken

> Obtain an authentication token for the user.

### NX_AuthenticationToken Parameters

| Name | Type | Description |
| --- | --- | --- |
| applicationName | string | Application name (e.g., 'appian') |
| deviceId | string | Device ID (e.g., 'designer') |
| deviceDescription | string | Device Description (e.g., 'appian integration') |
| permission | string | Read/write permissions () |

## Integration: NX_Automation

> Invoke Nuxeo automation endpoint

### NX_Automation Parameters

| Name | Type | Description |
| --- | --- | --- |
| input | string | Input document (or object), typically in the form of a document UUID (ecm:id) |
| params | LabelValue?list | Label/value list of parameters |
| automation | string | Automation Name (e.g., 'Document.Copy') |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_CreateFolderByID

> Create a child folder given a parent ID.

### NX_CreateFolderByID Parameters

| Name | Type | Description |
| --- | --- | --- |
| parent | string | Parent Document Path |
| name | string | Name of the thing |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_CreateFolderByPath

> Create a child folder given a parent path.

### NX_CreateFolderByPath Parameters

| Name | Type | Description |
| --- | --- | --- |
| parent | string | Parent Document Path |
| name | string | Name of the thing |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_CreateUploadBatch

> Creates and returns the "batchId" for the upload.

### NX_CreateUploadBatch Parameters

| Name | Type | Description |
| --- | --- | --- |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_DeleteDocumentByID

> Remove a document by UUID

### NX_DeleteDocumentByID Parameters

| Name | Type | Description |
| --- | --- | --- |
| id | string | Document Identifier (ecm:id) |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_DeleteDocumentByPath

> Remove a document by path

### NX_DeleteDocumentByPath Parameters

| Name | Type | Description |
| --- | --- | --- |
| path | string | Document Path |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_GetDocumentByID

> Retrieve a document by UUID

### NX_GetDocumentByID Parameters

| Name | Type | Description |
| --- | --- | --- |
| properties | string | Schema properties to return ('*' is everything) |
| id | string | Document Identifier (ecm:id) |
| enrichers | string | Enrich the document with additional data (https://doc.nuxeo.com/nxdoc/content-enrichers/) |

## Integration: NX_GetDocumentByPath

> Retrieve a document by Path

### NX_GetDocumentByPath Parameters

| Name | Type | Description |
| --- | --- | --- |
| properties | string | Schema properties to return ('*' is everything) |
| path | string | Document Path |
| enrichers | string | Enrich the document with additional data (https://doc.nuxeo.com/nxdoc/content-enrichers/) |

## Integration: NX_GetCurrentUser

> Get current user details

## Integration: NX_GetDocumentPDFPreview

> Retrieve a PDF preview of a document

### NX_GetDocumentPDFPreview Parameters

| Name | Type | Description |
| --- | --- | --- |
| id | string | Document Identifier (ecm:id) |

## Integration: NX_GetUserWorkspace

> Get the workspace for the current user

### NX_GetUserWorkspace Parameters

| Name | Type | Description |
| --- | --- | --- |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_GetDocumentAdapter

> Get the @adapter for a document.

### NX_GetDocumentAdapter Parameters

| Name | Type | Description |
| --- | --- | --- |
| id | string | Document Identifier (ecm:id) |
| adapter | string | Adapter name (e.g., 'preview') |

## Integration: NX_ListDocumentsByID

> List documents located in folder by parent ID.

### NX_ListDocumentsByID Parameters

| Name | Type | Description |
| --- | --- | --- |
| id | string | Document Identifier (ecm:id) |
| properties | string | Schema properties to return ('*' is everything) |

## Integration: NX_GetWorkflowInstances

> Get the list of active workflows.

## Integration: NX_ListDocumentsByPath

> List documents located in folder by parent path.

### NX_ListDocumentsByPath Parameters

| Name | Type | Description |
| --- | --- | --- |
| properties | string | Schema properties to return ('*' is everything) |
| path | string | Document Path |

## Integration: NX_MoveDocument

> Move document to a new path.

### NX_MoveDocument Parameters

| Name | Type | Description |
| --- | --- | --- |
| source | string | Source path |
| destination | string | Destination path |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_GetDocumentWorkflows

> Get the list of active workflows for a given document ID.

### NX_GetDocumentWorkflows Parameters

| Name | Type | Description |
| --- | --- | --- |
| id | string | Document Identifier (ecm:id) |

## Integration: NX_UpdateDocumentByID

> Update a document given an ID.

### NX_UpdateDocumentByID Parameters

| Name | Type | Description |
| --- | --- | --- |
| id | string | Document Identifier (ecm:id) |
| properties | LabelValue?list | Schema properties to return ('*' is everything) |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_SearchDocuments

> Search documents with NXQL (https://doc.nuxeo.com/nxdoc/nxql/).

### NX_SearchDocuments Parameters

| Name | Type | Description |
| --- | --- | --- |
| queryLanguage | string | Query language (e.g., 'NXQL') |
| query | string | NXQL query |
| pageSize | int | Page size |
| currentPageIndex | int | Current page index |

## Integration: NX_UpdateDocumentByPath

> Update a document given a path.

### NX_UpdateDocumentByPath Parameters

| Name | Type | Description |
| --- | --- | --- |
| path | string | Document Path |
| properties | LabelValue?list | Schema properties to return ('*' is everything) |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_CreateFileDocumentByPath

> Create a new document with content from an uploaded file.

### NX_CreateFileDocumentByPath Parameters

| Name | Type | Description |
| --- | --- | --- |
| parent | string | Parent Document Path |
| type | string | Type of the thing (e.g., 'File', 'Folder', or other document type) |
| name | string | Name of the thing |
| batchId | string | Batch ID, generated by 'NX_CreateUploadBatch' |
| fileIndex | string | File index, used for batch file uploads |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_FullTextSearch

> Perform [full text](https://doc.nuxeo.com/nxdoc/full-text-queries/) search.

### NX_FullTextSearch Parameters

| Name | Type | Description |
| --- | --- | --- |
| pageSize | int | Page size |
| currentPageIndex | int | Current page index |
| pageProvider | string | Page provider name |
| queryParams | string | Query parameters for page provider (Default: 'full_text_pp') |
| sortOrder | string | Sort order (ASC, DESC) |
| sortBy | string | Sort by column |
| schemas | string | Schemas to return (e.g., 'dublincore', 'files') |
| terms | string | Full text term search |

## Integration: NX_CreateDocumentByPath

> Create a document in a given path.

### NX_CreateDocumentByPath Parameters

| Name | Type | Description |
| --- | --- | --- |
| parent | string | Parent Document Path |
| name | string | Name of the thing |
| properties | LabelValue?list | Schema properties to return ('*' is everything) |
| type | string | Type of the thing (e.g., 'File', 'Folder', or other document type) |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_LinkAppianRecord

> Link Appian records and items to Nuxeo Documents.

### NX_LinkAppianRecord Parameters

| Name | Type | Description |
| --- | --- | --- |
| source | string | Source identifier |
| state | string | Document state |
| processes | string | Document processes |
| links | string | Link to the Appian record |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_SearchPageProvider

> Execute page provider.

### NX_SearchPageProvider Parameters

| Name | Type | Description |
| --- | --- | --- |
| pageSize | int | Page size |
| currentPageIndex | int | Current page index |
| pageProvider | string | Page provider name |
| queryParams | string | Query parameters |
| sortOrder | string | Sort order (ASC, DESC) |
| sortBy | string | Sort by column name |

## Integration: NX_UploadFileContent

> Upload a file content, requires a "batchId".

### NX_UploadFileContent Parameters

| Name | Type | Description |
| --- | --- | --- |
| batchId | string | Batch ID, generated by 'NX_CreateUploadBatch' |
| fileNumber | string | File number for batch upload |
| fileName | string | File name |
| fileType | string | File mime-type |
| content | CollaborationDocument | Binary file content |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |
