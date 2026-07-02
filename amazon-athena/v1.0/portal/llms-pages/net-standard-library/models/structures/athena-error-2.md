# Athena Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkF0aGVuYUVycm9yMg

*This model accepts additional fields of type object.*


# Class Name

`AthenaError2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ErrorCategory` | `int?` | Optional | **Constraints**: `>= 1`, `<= 3` |
| `ErrorType` | `int?` | Optional | **Constraints**: `>= 0`, `<= 9999` |
| `Retryable` | `bool?` | Optional | - |
| `ErrorMessage` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

AthenaError2 athenaError2 = new AthenaError2
{
    ErrorCategory = 3,
    ErrorType = 56,
    Retryable = false,
    ErrorMessage = "ErrorMessage0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



