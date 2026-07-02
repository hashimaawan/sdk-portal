# Result Reuse Information

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24

Contains information about whether the result of a previous query was reused.

*This model accepts additional fields of type object.*


# Class Name

`ResultReuseInformation`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ReusedPreviousResult` | `bool` | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ResultReuseInformation resultReuseInformation = new ResultReuseInformation
{
    ReusedPreviousResult = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



