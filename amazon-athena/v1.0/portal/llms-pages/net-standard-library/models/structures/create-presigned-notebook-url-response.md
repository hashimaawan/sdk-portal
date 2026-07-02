# Create Presigned Notebook Url Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVzcG9uc2U

*This model accepts additional fields of type object.*


# Class Name

`CreatePresignedNotebookUrlResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookUrl` | `string` | Required | - |
| `AuthToken` | `string` | Required | **Constraints**: *Maximum Length*: `2048` |
| `AuthTokenExpirationTime` | `int` | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

CreatePresignedNotebookUrlResponse createPresignedNotebookUrlResponse = new CreatePresignedNotebookUrlResponse
{
    NotebookUrl = "NotebookUrl0",
    AuthToken = "AuthToken4",
    AuthTokenExpirationTime = 240,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



