# Region

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlZ2lvbg

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Region`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available` | `bool` | Required | This is a boolean value that represents whether new Droplets can be created in this region. |
| `features` | `List[str]` | Required | This attribute is set to an array which contains features available in this region |
| `name` | `str` | Required | The display name of the region.  This will be a full name that is used in the control panel and other interfaces. |
| `sizes` | `List[str]` | Required | This attribute is set to an array which contains the identifying slugs for the sizes available in this region. |
| `slug` | `str` | Required | A human-readable string that is used as a unique identifier for each region. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.region import Region

region = Region(
    available=True,
    features=[
        'private_networking',
        'backups',
        'ipv6',
        'metadata',
        'install_agent',
        'storage',
        'image_transfer'
    ],
    name='New York 3',
    sizes=[
        's-1vcpu-1gb',
        's-1vcpu-2gb',
        's-1vcpu-3gb',
        's-2vcpu-2gb',
        's-3vcpu-1gb',
        's-2vcpu-4gb',
        's-4vcpu-8gb',
        's-6vcpu-16gb',
        's-8vcpu-32gb',
        's-12vcpu-48gb',
        's-16vcpu-64gb',
        's-20vcpu-96gb',
        's-24vcpu-128gb',
        's-32vcpu-192g'
    ],
    slug='nyc3',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



