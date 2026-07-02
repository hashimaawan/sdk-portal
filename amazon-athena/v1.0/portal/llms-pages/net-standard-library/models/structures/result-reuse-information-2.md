# Result Reuse Information 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24y

*This model accepts additional fields of type object.*


# Class Name

`ResultReuseInformation2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ReusedPreviousResult` | `bool` | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ResultReuseInformation2 resultReuseInformation2 = new ResultReuseInformation2
{
    ReusedPreviousResult = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



