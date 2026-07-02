# Databases

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdGFiYXNlcw

Tagged Resource Statistics include metadata regarding the resource type that has been tagged.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Databases`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Count` | `int?` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` |
| `LastTaggedUri` | `string` | Optional | The URI for the last tagged object for this type of resource. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Databases databases = new Databases
{
    Count = 5,
    LastTaggedUri = "https://api.digitalocean.com/v2/images/7555620",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



