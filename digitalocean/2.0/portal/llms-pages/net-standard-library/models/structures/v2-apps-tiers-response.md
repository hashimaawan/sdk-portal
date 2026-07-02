# V2 Apps Tiers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2AppsTiersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tiers` | [`List<Tier>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/tier.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2AppsTiersResponse v2AppsTiersResponse = new V2AppsTiersResponse
{
    Tiers = new List<Tier>
    {
        new Tier
        {
            BuildSeconds = "build_seconds4",
            EgressBandwidthBytes = "egress_bandwidth_bytes2",
            Name = "name8",
            Slug = "slug8",
            StorageBytes = "storage_bytes4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Tier
        {
            BuildSeconds = "build_seconds4",
            EgressBandwidthBytes = "egress_bandwidth_bytes2",
            Name = "name8",
            Slug = "slug8",
            StorageBytes = "storage_bytes4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Tier
        {
            BuildSeconds = "build_seconds4",
            EgressBandwidthBytes = "egress_bandwidth_bytes2",
            Name = "name8",
            Slug = "slug8",
            StorageBytes = "storage_bytes4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



