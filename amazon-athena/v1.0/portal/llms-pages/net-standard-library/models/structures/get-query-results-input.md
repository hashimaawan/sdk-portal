# Get Query Results Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c0lucHV0

*This model accepts additional fields of type object.*


# Class Name

`GetQueryResultsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 1`, `<= 1000` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

GetQueryResultsInput getQueryResultsInput = new GetQueryResultsInput
{
    QueryExecutionId = "QueryExecutionId6",
    NextToken = "NextToken2",
    MaxResults = 42,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



