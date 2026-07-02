# V2 Apps Regions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZWdpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsRegionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `regions` | [`List[GeographicalInformationAboutAnAppOrigin]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/geographical-information-about-an-app-origin.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.geographical_information_about_an_app_origin import GeographicalInformationAboutAnAppOrigin
from digitaloceanapi.models.v_2_apps_regions_response import V2AppsRegionsResponse

v_2_apps_regions_response = V2AppsRegionsResponse(
    regions=[
        GeographicalInformationAboutAnAppOrigin(
            continent='continent2',
            data_centers=[
                'data_centers9'
            ],
            default=False,
            disabled=False,
            flag='flag4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        GeographicalInformationAboutAnAppOrigin(
            continent='continent2',
            data_centers=[
                'data_centers9'
            ],
            default=False,
            disabled=False,
            flag='flag4',
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



