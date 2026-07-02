# Options 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRk9wdGlvbnMx

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Options1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `regions` | [`List[Region4]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/region-4.md) | Optional | - |
| `sizes` | [`List[Size1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/size-1.md) | Optional | - |
| `versions` | [`List[AvailableUpgradeVersion]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/available-upgrade-version.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.available_upgrade_version import AvailableUpgradeVersion
from digitaloceanapi.models.options_1 import Options1
from digitaloceanapi.models.region_4 import Region4
from digitaloceanapi.models.size_1 import Size1

options_1 = Options1(
    regions=[
        Region4(
            name='name0',
            slug='slug6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Region4(
            name='name0',
            slug='slug6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    sizes=[
        Size1(
            name='name0',
            slug='slug6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Size1(
            name='name0',
            slug='slug6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Size1(
            name='name0',
            slug='slug6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    versions=[
        AvailableUpgradeVersion(
            kubernetes_version='kubernetes_version6',
            slug='slug4',
            supported_features=[
                'supported_features7',
                'supported_features8'
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        AvailableUpgradeVersion(
            kubernetes_version='kubernetes_version6',
            slug='slug4',
            supported_features=[
                'supported_features7',
                'supported_features8'
            ],
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



