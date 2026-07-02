# V2 Droplets Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing information about a resource to be scheduled for deletion.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floating_ips` | `List[str]` | Optional | An array of unique identifiers for the floating IPs to be scheduled for deletion. |
| `reserved_ips` | `List[str]` | Optional | An array of unique identifiers for the reserved IPs to be scheduled for deletion. |
| `snapshots` | `List[str]` | Optional | An array of unique identifiers for the snapshots to be scheduled for deletion. |
| `volume_snapshots` | `List[str]` | Optional | An array of unique identifiers for the volume snapshots to be scheduled for deletion. |
| `volumes` | `List[str]` | Optional | An array of unique identifiers for the volumes to be scheduled for deletion. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_2_droplets_destroy_with_associated_resources_selective_request import V2DropletsDestroyWithAssociatedResourcesSelectiveRequest

v_2_droplets_destroy_with_associated_resources_selective_request = V2DropletsDestroyWithAssociatedResourcesSelectiveRequest(
    floating_ips=[
        '6186916'
    ],
    reserved_ips=[
        '6186916'
    ],
    snapshots=[
        '61486916'
    ],
    volume_snapshots=[
        'edb0478d-7436-11ea-86e6-0a58ac144b91'
    ],
    volumes=[
        'ba49449a-7435-11ea-b89e-0a58ac14480f'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



