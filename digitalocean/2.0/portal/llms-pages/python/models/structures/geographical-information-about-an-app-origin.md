# Geographical Information about an App Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkdlb2dyYXBoaWNhbCUyNTIwaW5mb3JtYXRpb24lMjUyMGFib3V0JTI1MjBhbiUyNTIwYXBwJTI1MjBvcmlnaW4

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`GeographicalInformationAboutAnAppOrigin`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `continent` | `str` | Optional, Read-only | - |
| `data_centers` | `List[str]` | Optional, Read-only | - |
| `default` | `bool` | Optional, Read-only | Whether or not the region is presented as the default. |
| `disabled` | `bool` | Optional, Read-only | - |
| `flag` | `str` | Optional, Read-only | - |
| `label` | `str` | Optional, Read-only | - |
| `reason` | `str` | Optional, Read-only | - |
| `slug` | `str` | Optional, Read-only | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.geographical_information_about_an_app_origin import GeographicalInformationAboutAnAppOrigin

geographical_information_about_an_app_origin = GeographicalInformationAboutAnAppOrigin(
    continent='europe',
    data_centers=[
        'ams'
    ],
    default=True,
    disabled=True,
    flag='ams',
    label='ams',
    reason='to crowded',
    slug='basic',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



