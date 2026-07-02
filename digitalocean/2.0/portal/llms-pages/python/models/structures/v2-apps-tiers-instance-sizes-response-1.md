# V2 Apps Tiers Instance Sizes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwSW5zdGFuY2UlMjUyMFNpemVzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsTiersInstanceSizesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `instance_size` | [`InstanceSize`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/instance-size.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.instance_size import InstanceSize
from digitaloceanapi.models.m_shared_shared_vcpu_cores_dedicated_dedicated_vcpu_cores import MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores
from digitaloceanapi.models.v_2_apps_tiers_instance_sizes_response_1 import V2AppsTiersInstanceSizesResponse1

v_2_apps_tiers_instance_sizes_response_1 = V2AppsTiersInstanceSizesResponse1(
    instance_size=InstanceSize(
        cpu_type=MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.DEDICATED,
        cpus='cpus4',
        memory_bytes='memory_bytes8',
        name='name8',
        slug='slug2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



