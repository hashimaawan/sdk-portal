# List Query Executions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RRdWVyeUV4ZWN1dGlvbnNPdXRwdXQ

*This model accepts additional fields of type object.*


# Class Name

`ListQueryExecutionsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutionIds` | `List<string>` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

ListQueryExecutionsOutput listQueryExecutionsOutput = new ListQueryExecutionsOutput
{
    QueryExecutionIds = new List<string>
    {
        "QueryExecutionIds9",
    },
    NextToken = "NextToken2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



