# V2 Apps Tiers Instance Sizes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwSW5zdGFuY2UlMjUyMFNpemVzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2AppsTiersInstanceSizesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `InstanceSize` | [`InstanceSize`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/instance-size.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

V2AppsTiersInstanceSizesResponse1 v2AppsTiersInstanceSizesResponse1 = new V2AppsTiersInstanceSizesResponse1
{
    InstanceSize = new InstanceSize
    {
        CpuType = MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.Dedicated,
        Cpus = "cpus4",
        MemoryBytes = "memory_bytes8",
        Name = "name8",
        Slug = "slug2",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



