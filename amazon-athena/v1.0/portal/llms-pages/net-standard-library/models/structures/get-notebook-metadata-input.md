# Get Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldE5vdGVib29rTWV0YWRhdGFJbnB1dA

*This model accepts additional fields of type object.*


# Class Name

`GetNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

GetNotebookMetadataInput getNotebookMetadataInput = new GetNotebookMetadataInput
{
    NotebookId = "NotebookId0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



