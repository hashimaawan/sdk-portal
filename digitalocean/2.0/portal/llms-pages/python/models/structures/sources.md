# Sources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlNvdXJjZXM

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Sources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `addresses` | `List[str]` | Optional | An array of strings containing the IPv4 addresses, IPv6 addresses, IPv4 CIDRs, and/or IPv6 CIDRs to which the firewall will allow traffic. |
| `droplet_ids` | `List[int]` | Optional | An array containing the IDs of the Droplets to which the firewall will allow traffic. |
| `kubernetes_ids` | `List[str]` | Optional | An array containing the IDs of the Kubernetes clusters to which the firewall will allow traffic. |
| `load_balancer_uids` | `List[str]` | Optional | An array containing the IDs of the load balancers to which the firewall will allow traffic. |
| `tags` | `List[str]` | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.sources import Sources

sources = Sources(
    addresses=[
        '1.2.3.4',
        '18.0.0.0/8'
    ],
    droplet_ids=[
        8043964
    ],
    kubernetes_ids=[
        '41b74c5d-9bd0-5555-5555-a57c495b81a3'
    ],
    load_balancer_uids=[
        '4de7ac8b-495b-4884-9a69-1050c6793cd6'
    ],
    tags=[
        'tags1',
        'tags2',
        'tags3'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



