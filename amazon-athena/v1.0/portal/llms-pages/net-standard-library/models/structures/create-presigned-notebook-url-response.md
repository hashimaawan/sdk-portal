# Create Presigned Notebook Url Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVzcG9uc2U


# Class Name

`CreatePresignedNotebookUrlResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookUrl` | `string` | Required | - |
| `AuthToken` | `string` | Required | **Constraints**: *Maximum Length*: `2048` |
| `AuthTokenExpirationTime` | `int` | Required | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

CreatePresignedNotebookUrlResponse createPresignedNotebookUrlResponse = new CreatePresignedNotebookUrlResponse
{
    NotebookUrl = "NotebookUrl0",
    AuthToken = "AuthToken4",
    AuthTokenExpirationTime = 240,
};
```



