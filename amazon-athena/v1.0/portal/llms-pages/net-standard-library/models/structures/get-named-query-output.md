# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ

*This model accepts additional fields of type object.*


# Class Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQuery` | [`NamedQuery1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/named-query-1.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

GetNamedQueryOutput getNamedQueryOutput = new GetNamedQueryOutput
{
    NamedQuery = new NamedQuery1
    {
        Name = "Name0",
        Database = "Database8",
        QueryString = "QueryString2",
        Description = "Description6",
        NamedQueryId = "NamedQueryId2",
        WorkGroup = "WorkGroup2",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



