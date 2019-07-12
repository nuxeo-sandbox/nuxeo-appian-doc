# Nuxeo Appian Application Integrations

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

## Integration: NX_AuthenticationToken

> Obtain an authentication token for the user.

### NX_AuthenticationToken Parameters

| Name | Type | Description |
| --- | --- | --- |
| applicationName | string |  |
| deviceId | string |  |
| deviceDescription | string |  |
| permission | string |  |

## Integration: NX_Automation

> Invoke Nuxeo automation endpoint

### NX_Automation Parameters

| Name | Type | Description |
| --- | --- | --- |
| input | string |  |
| params | LabelValue?list |  |
| automation | string |  |
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
| adapter | string |  |

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
| source | string |  |
| destination | string |  |
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
| queryLanguage | string |  |
| query | string |  |
| pageSize | int |  |
| currentPageIndex | int |  |

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
| batchId | string |  |
| fileIndex | string |  |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_FullTextSearch

> Perform full text search.

### NX_FullTextSearch Parameters

| Name | Type | Description |
| --- | --- | --- |
| pageSize | int |  |
| currentPageIndex | int |  |
| pageProvider | string |  |
| queryParams | string |  |
| sortOrder | string |  |
| sortBy | string |  |
| schemas | string |  |
| terms | string |  |

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
| source | string |  |
| state | string |  |
| processes | string |  |
| links | string |  |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |

## Integration: NX_SearchPageProvider

> Execute page provider.

### NX_SearchPageProvider Parameters

| Name | Type | Description |
| --- | --- | --- |
| pageSize | int |  |
| currentPageIndex | int |  |
| pageProvider | string |  |
| queryParams | string |  |
| sortOrder | string |  |
| sortBy | string |  |

## Integration: NX_UploadFileContent

> Upload a file content, requires a "batchId".

### NX_UploadFileContent Parameters

| Name | Type | Description |
| --- | --- | --- |
| batchId | string |  |
| fileNumber | string |  |
| fileName | string |  |
| fileType | string |  |
| content | CollaborationDocument |  |
| onSuccess | Variant | Successful event |
| onError | Variant | Error event |
