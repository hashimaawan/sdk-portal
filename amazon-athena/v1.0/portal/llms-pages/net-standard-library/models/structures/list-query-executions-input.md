# List Query Executions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RRdWVyeUV4ZWN1dGlvbnNJbnB1dA

*This model accepts additional fields of type object.*


# Class Name

`ListQueryExecutionsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 0`, `<= 50` |
| `WorkGroup` | `string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ListQueryExecutionsInput listQueryExecutionsInput = new ListQueryExecutionsInput
{
    NextToken = "NextToken2",
    MaxResults = 34,
    WorkGroup = "WorkGroup4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



