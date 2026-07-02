# Instance Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkluc3RhbmNlU2l6ZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`InstanceSize`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CpuType` | [`MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/shared-shared-v-cpu-cores-dedicated-dedicated-v-cpu-cores.md) | Optional | **Default**: `MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.UNSPECIFIED` |
| `Cpus` | `string` | Optional | - |
| `MemoryBytes` | `string` | Optional | - |
| `Name` | `string` | Optional | - |
| `Slug` | `string` | Optional | - |
| `TierDowngradeTo` | `string` | Optional | - |
| `TierSlug` | `string` | Optional | - |
| `TierUpgradeTo` | `string` | Optional | - |
| `UsdPerMonth` | `string` | Optional | - |
| `UsdPerSecond` | `string` | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

InstanceSize instanceSize = new InstanceSize
{
    CpuType = MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.Shared,
    Cpus = "3",
    MemoryBytes = "1048",
    Name = "name",
    Slug = "basic",
    TierDowngradeTo = "basic",
    TierSlug = "basic",
    TierUpgradeTo = "basic",
    UsdPerMonth = "23",
    UsdPerSecond = "0.00000001232",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



