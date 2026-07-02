# V2 Firewalls Droplets Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMERyb3BsZXRzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2FirewallsDropletsRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet_ids` | `List[int]` | Required | An array containing the IDs of the Droplets to be assigned to the firewall. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_2_firewalls_droplets_request_1 import V2FirewallsDropletsRequest1

v_2_firewalls_droplets_request_1 = V2FirewallsDropletsRequest1(
    droplet_ids=[
        49696269
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



