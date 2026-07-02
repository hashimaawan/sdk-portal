# V2 Apps Tiers Instance Sizes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwSW5zdGFuY2UlMjUyMFNpemVzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2AppsTiersInstanceSizesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DiscountPercent` | `double?` | Optional | - |
| `InstanceSizes` | [`List<InstanceSize>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/instance-size.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2AppsTiersInstanceSizesResponse v2AppsTiersInstanceSizesResponse = new V2AppsTiersInstanceSizesResponse
{
    DiscountPercent = 2.32,
    InstanceSizes = new List<InstanceSize>
    {
        new InstanceSize
        {
            CpuType = MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.Dedicated,
            Cpus = "cpus4",
            MemoryBytes = "memory_bytes8",
            Name = "name8",
            Slug = "slug8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



