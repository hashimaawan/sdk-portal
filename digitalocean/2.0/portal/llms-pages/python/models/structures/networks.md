# Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRk5ldHdvcmtz

The details of the network that are configured for the Droplet instance.  This is an object that contains keys for IPv4 and IPv6.  The value of each of these is an array that contains objects describing an individual IP resource allocated to the Droplet.  These will define attributes like the IP address, netmask, and gateway of the specific network depending on the type of network it is.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Networks`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `v_4` | [`List[V4]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v4.md) | Optional | - |
| `v_6` | [`List[V6]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v6.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.networks import Networks
from digitaloceanapi.models.type_10 import Type10
from digitaloceanapi.models.type_11 import Type11
from digitaloceanapi.models.v_4 import V4
from digitaloceanapi.models.v_6 import V6

networks = Networks(
    v_4=[
        V4(
            gateway='gateway2',
            ip_address='ip_address2',
            netmask='netmask2',
            mtype=Type10.PUBLIC,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        V4(
            gateway='gateway2',
            ip_address='ip_address2',
            netmask='netmask2',
            mtype=Type10.PUBLIC,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        V4(
            gateway='gateway2',
            ip_address='ip_address2',
            netmask='netmask2',
            mtype=Type10.PUBLIC,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    v_6=[
        V6(
            gateway='gateway4',
            ip_address='ip_address4',
            netmask=106,
            mtype=Type11.PUBLIC,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        V6(
            gateway='gateway4',
            ip_address='ip_address4',
            netmask=106,
            mtype=Type11.PUBLIC,
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



