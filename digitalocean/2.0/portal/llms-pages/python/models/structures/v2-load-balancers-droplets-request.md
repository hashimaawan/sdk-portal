# V2 Load Balancers Droplets Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMERyb3BsZXRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2LoadBalancersDropletsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet_ids` | `List[int]` | Optional | An array containing the IDs of the Droplets assigned to the load balancer. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_2_load_balancers_droplets_request import V2LoadBalancersDropletsRequest

v_2_load_balancers_droplets_request = V2LoadBalancersDropletsRequest(
    droplet_ids=[
        3164444,
        3164445
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



