# V2 Registry Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwT3B0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2RegistryOptionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Options` | [`Options2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/options-2.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2RegistryOptionsResponse v2RegistryOptionsResponse = new V2RegistryOptionsResponse
{
    Options = new Options2
    {
        AvailableRegions = new List<string>
        {
            "available_regions9",
        },
        SubscriptionTiers = new List<SubscriptionTier>
        {
            new SubscriptionTier
            {
                AllowStorageOverage = false,
                IncludedBandwidthBytes = 172L,
                IncludedRepositories = 194,
                IncludedStorageBytes = 242L,
                MonthlyPriceInCents = 236,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new SubscriptionTier
            {
                AllowStorageOverage = false,
                IncludedBandwidthBytes = 172L,
                IncludedRepositories = 194,
                IncludedStorageBytes = 242L,
                MonthlyPriceInCents = 236,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new SubscriptionTier
            {
                AllowStorageOverage = false,
                IncludedBandwidthBytes = 172L,
                IncludedRepositories = 194,
                IncludedStorageBytes = 242L,
                MonthlyPriceInCents = 236,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



