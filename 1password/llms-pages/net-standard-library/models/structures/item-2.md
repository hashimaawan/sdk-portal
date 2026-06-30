# Item 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRkl0ZW0y

*This model accepts additional fields of type object.*


# Class Name

`Item2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;

Item2 item2 = new Item2
{
    Id = "id2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



