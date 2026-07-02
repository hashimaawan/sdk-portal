# Instance Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkluc3RhbmNlU2l6ZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`InstanceSize`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cpu_type` | [`MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/shared-shared-v-cpu-cores-dedicated-dedicated-v-cpu-cores.md) | Optional | **Default**: `"UNSPECIFIED"` |
| `cpus` | `str` | Optional | - |
| `memory_bytes` | `str` | Optional | - |
| `name` | `str` | Optional | - |
| `slug` | `str` | Optional | - |
| `tier_downgrade_to` | `str` | Optional | - |
| `tier_slug` | `str` | Optional | - |
| `tier_upgrade_to` | `str` | Optional | - |
| `usd_per_month` | `str` | Optional | - |
| `usd_per_second` | `str` | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.instance_size import InstanceSize
from digitaloceanapi.models.m_shared_shared_vcpu_cores_dedicated_dedicated_vcpu_cores import MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores

instance_size = InstanceSize(
    cpu_type=MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.SHARED,
    cpus='3',
    memory_bytes='1048',
    name='name',
    slug='basic',
    tier_downgrade_to='basic',
    tier_slug='basic',
    tier_upgrade_to='basic',
    usd_per_month='23',
    usd_per_second='0.00000001232',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



