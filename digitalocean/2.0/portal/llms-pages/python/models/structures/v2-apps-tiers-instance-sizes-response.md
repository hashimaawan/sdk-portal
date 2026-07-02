# V2 Apps Tiers Instance Sizes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwSW5zdGFuY2UlMjUyMFNpemVzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsTiersInstanceSizesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `discount_percent` | `float` | Optional | - |
| `instance_sizes` | [`List[InstanceSize]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/instance-size.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.instance_size import InstanceSize
from digitaloceanapi.models.m_shared_shared_vcpu_cores_dedicated_dedicated_vcpu_cores import MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores
from digitaloceanapi.models.v_2_apps_tiers_instance_sizes_response import V2AppsTiersInstanceSizesResponse

v_2_apps_tiers_instance_sizes_response = V2AppsTiersInstanceSizesResponse(
    discount_percent=2.32,
    instance_sizes=[
        InstanceSize(
            cpu_type=MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.DEDICATED,
            cpus='cpus4',
            memory_bytes='memory_bytes8',
            name='name8',
            slug='slug8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        InstanceSize(
            cpu_type=MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.DEDICATED,
            cpus='cpus4',
            memory_bytes='memory_bytes8',
            name='name8',
            slug='slug8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



