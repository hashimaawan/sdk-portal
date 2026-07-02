# List Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhSW5wdXQ

*This model accepts additional fields of type object.*


# Class Name

`ListNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Filters` | [`Filters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/filters.md) | Optional | - |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ListNotebookMetadataInput listNotebookMetadataInput = new ListNotebookMetadataInput
{
    WorkGroup = "WorkGroup4",
    Filters = new Filters
    {
        Name = "Name2",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    NextToken = "NextToken2",
    MaxResults = 50,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



