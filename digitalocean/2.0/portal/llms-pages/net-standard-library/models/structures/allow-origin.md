# Allow Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFsbG93T3JpZ2lu

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`AllowOrigin`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Exact` | `string` | Optional | Exact string match. Only 1 of `exact`, `prefix`, or `regex` must be set.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Prefix` | `string` | Optional | Prefix-based match. Only 1 of `exact`, `prefix`, or `regex` must be set.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Regex` | `string` | Optional | RE2 style regex-based match. Only 1 of `exact`, `prefix`, or `regex` must be set. For more information about RE2 syntax, see: https://github.com/google/re2/wiki/Syntax<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

AllowOrigin allowOrigin = new AllowOrigin
{
    Exact = "https://www.example.com",
    Prefix = "https://www.example.com",
    Regex = "^.*example.com",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



