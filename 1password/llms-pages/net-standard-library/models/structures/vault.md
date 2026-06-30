# Vault

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRlZhdWx0

*This model accepts additional fields of type object.*


# Class Name

`Vault`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AttributeVersion` | `int?` | Optional | The vault version |
| `ContentVersion` | `int?` | Optional | The version of the vault contents |
| `CreatedAt` | `DateTime?` | Optional, Read-only | - |
| `Description` | `string` | Optional | - |
| `Id` | `string` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `Items` | `int?` | Optional | Number of active items in the vault |
| `Name` | `string` | Optional | - |
| `Type` | [`Type2?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/enumerations/type-2.md) | Optional | - |
| `UpdatedAt` | `DateTime?` | Optional, Read-only | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;
using System.Globalization;

Vault vault = new Vault
{
    AttributeVersion = 108,
    ContentVersion = 228,
    CreatedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Description = "description6",
    Id = "id6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



