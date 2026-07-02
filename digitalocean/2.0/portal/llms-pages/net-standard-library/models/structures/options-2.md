# Options 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk9wdGlvbnMy

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Options2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AvailableRegions` | `List<string>` | Optional | - |
| `SubscriptionTiers` | [`List<SubscriptionTier>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/subscription-tier.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Options2 options2 = new Options2
{
    AvailableRegions = new List<string>
    {
        "nyc3",
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
};
```



