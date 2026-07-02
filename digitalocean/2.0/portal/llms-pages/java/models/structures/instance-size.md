# Instance Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkluc3RhbmNlU2l6ZQ

*This model accepts additional fields of type Object.*


# Class Name

`InstanceSize`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CpuType` | [`MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/shared-shared-v-cpu-cores-dedicated-dedicated-v-cpu-cores.md) | Optional | **Default**: `MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.UNSPECIFIED` | MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores getCpuType() | setCpuType(MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores cpuType) |
| `Cpus` | `String` | Optional | - | String getCpus() | setCpus(String cpus) |
| `MemoryBytes` | `String` | Optional | - | String getMemoryBytes() | setMemoryBytes(String memoryBytes) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Slug` | `String` | Optional | - | String getSlug() | setSlug(String slug) |
| `TierDowngradeTo` | `String` | Optional | - | String getTierDowngradeTo() | setTierDowngradeTo(String tierDowngradeTo) |
| `TierSlug` | `String` | Optional | - | String getTierSlug() | setTierSlug(String tierSlug) |
| `TierUpgradeTo` | `String` | Optional | - | String getTierUpgradeTo() | setTierUpgradeTo(String tierUpgradeTo) |
| `UsdPerMonth` | `String` | Optional | - | String getUsdPerMonth() | setUsdPerMonth(String usdPerMonth) |
| `UsdPerSecond` | `String` | Optional | - | String getUsdPerSecond() | setUsdPerSecond(String usdPerSecond) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.InstanceSize;
import com.digitalocean.api.models.MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores;
import java.io.IOException;

InstanceSize instanceSize = new InstanceSize.Builder()
    .cpuType(MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.SHARED)
    .cpus("3")
    .memoryBytes("1048")
    .name("name")
    .slug("basic")
    .tierDowngradeTo("basic")
    .tierSlug("basic")
    .tierUpgradeTo("basic")
    .usdPerMonth("23")
    .usdPerSecond("0.00000001232")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



