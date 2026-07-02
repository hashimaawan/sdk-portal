# Tier

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRpZXI

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Tier`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BuildSeconds` | `string` | Optional | - |
| `EgressBandwidthBytes` | `string` | Optional | - |
| `Name` | `string` | Optional | - |
| `Slug` | `string` | Optional | - |
| `StorageBytes` | `string` | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Tier tier = new Tier
{
    BuildSeconds = "233",
    EgressBandwidthBytes = "123",
    Name = "test",
    Slug = "test",
    StorageBytes = "10000000",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



