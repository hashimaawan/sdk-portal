# Section 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRlNlY3Rpb24y

*This model accepts additional fields of type object.*


# Class Name

`Section2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | - |
| `Label` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;

Section2 section2 = new Section2
{
    Id = "id4",
    Label = "label4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



