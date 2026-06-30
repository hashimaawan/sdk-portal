# Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRkl0ZW0

*This model accepts additional fields of type object.*


# Class Name

`Item`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Category` | [`Category`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/enumerations/category.md) | Required | - |
| `CreatedAt` | `DateTime?` | Optional, Read-only | - |
| `Favorite` | `bool?` | Optional | **Default**: `false` |
| `Id` | `string` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `LastEditedBy` | `string` | Optional, Read-only | - |
| `State` | [`State?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/enumerations/state.md) | Optional, Read-only | - |
| `Tags` | `List<string>` | Optional | - |
| `Title` | `string` | Optional | - |
| `UpdatedAt` | `DateTime?` | Optional, Read-only | - |
| `Urls` | [`List<Url>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/url.md) | Optional | - |
| `Vault` | [`Vault1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/vault-1.md) | Required | - |
| `Version` | `int?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

Item item = new Item
{
    Category = Category.SshKey,
    Vault = new Vault1
    {
        Id = "id6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    CreatedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Favorite = false,
    Id = "id2",
    LastEditedBy = "lastEditedBy8",
    State = State.Archived,
    Urls = new List<Url>
    {
        new Url
        {
            Href = "https://example.com",
            Primary = true,
        },
        new Url
        {
            Href = "https://example.org",
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



