# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRlJlc291cmNl

*This model accepts additional fields of type object.*


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Item` | [`Item2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/item-2.md) | Optional | - |
| `ItemVersion` | `int?` | Optional | - |
| `Type` | [`Type?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/enumerations/type.md) | Optional | - |
| `Vault` | [`Vault3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/vault-3.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;

Resource resource = new Resource
{
    Item = new Item2
    {
        Id = "id2",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ItemVersion = 108,
    Type = M1PasswordConnect.Standard.Models.Type.Item,
    Vault = new Vault3
    {
        Id = "id6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



