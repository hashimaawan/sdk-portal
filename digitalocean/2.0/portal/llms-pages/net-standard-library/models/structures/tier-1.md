# Tier 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRpZXIx

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Tier1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AllowStorageOverage` | `bool?` | Optional | A boolean indicating whether the subscription tier supports additional storage above what is included in the base plan at an additional cost per GiB used. |
| `IncludedBandwidthBytes` | `long?` | Optional | The amount of outbound data transfer included in the subscription tier in bytes. |
| `IncludedRepositories` | `int?` | Optional | The number of repositories included in the subscription tier. `0` indicates that the subscription tier includes unlimited repositories. |
| `IncludedStorageBytes` | `long?` | Optional | The amount of storage included in the subscription tier in bytes. |
| `MonthlyPriceInCents` | `int?` | Optional | The monthly cost of the subscription tier in cents. |
| `Name` | `string` | Optional | The name of the subscription tier. |
| `Slug` | `string` | Optional | The slug identifier of the subscription tier. |
| `StorageOveragePriceInCents` | `int?` | Optional | The price paid in cents per GiB for additional storage beyond what is included in the subscription plan. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Tier1 tier1 = new Tier1
{
    AllowStorageOverage = true,
    IncludedBandwidthBytes = 5368709120L,
    IncludedRepositories = 5,
    IncludedStorageBytes = 5368709120L,
    MonthlyPriceInCents = 500,
    Name = "Basic",
    Slug = "basic",
    StorageOveragePriceInCents = 2,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



