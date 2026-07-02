# Result Reuse by Age Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9uMg

*This model accepts additional fields of type object.*


# Class Name

`ResultReuseByAgeConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Enabled` | `bool` | Required | - |
| `MaxAgeInMinutes` | `int?` | Optional | **Constraints**: `>= 0`, `<= 10080` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ResultReuseByAgeConfiguration2 resultReuseByAgeConfiguration2 = new ResultReuseByAgeConfiguration2
{
    Enabled = false,
    MaxAgeInMinutes = 44,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



