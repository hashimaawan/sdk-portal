# Vault 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRlZhdWx0Mw

*This model accepts additional fields of type object.*


# Class Name

`Vault3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;

Vault3 vault3 = new Vault3
{
    Id = "id0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



