# Section

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRlNlY3Rpb24

*This model accepts additional fields of type object.*


# Class Name

`Section`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;

Section section = new Section
{
    Id = "id6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



