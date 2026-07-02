# V2 Databases Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9wdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesOptionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `options` | [`Options`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/options.md) | Optional | - |
| `version_availability` | [`VersionAvailability`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/version-availability.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.layout import Layout
from digitaloceanapi.models.mongodb import Mongodb
from digitaloceanapi.models.mongodb_1 import Mongodb1
from digitaloceanapi.models.mysql import Mysql
from digitaloceanapi.models.options import Options
from digitaloceanapi.models.pg import Pg
from digitaloceanapi.models.redis import Redis
from digitaloceanapi.models.v_2_databases_options_response import V2DatabasesOptionsResponse
from digitaloceanapi.models.version_availability import VersionAvailability

v_2_databases_options_response = V2DatabasesOptionsResponse(
    options=Options(
        mongodb=Mongodb(
            regions=[
                'regions3',
                'regions4'
            ],
            versions=[
                'versions3',
                'versions4'
            ],
            layouts=[
                Layout(
                    num_nodes=190,
                    sizes=[
                        'sizes2',
                        'sizes3'
                    ],
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                Layout(
                    num_nodes=190,
                    sizes=[
                        'sizes2',
                        'sizes3'
                    ],
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        mysql=Mysql(
            regions=[
                'regions9',
                'regions0',
                'regions1'
            ],
            versions=[
                'versions9',
                'versions0',
                'versions1'
            ],
            layouts=[
                Layout(
                    num_nodes=190,
                    sizes=[
                        'sizes2',
                        'sizes3'
                    ],
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                Layout(
                    num_nodes=190,
                    sizes=[
                        'sizes2',
                        'sizes3'
                    ],
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                Layout(
                    num_nodes=190,
                    sizes=[
                        'sizes2',
                        'sizes3'
                    ],
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        pg=Pg(
            regions=[
                'regions3'
            ],
            versions=[
                'versions3'
            ],
            layouts=[
                Layout(
                    num_nodes=190,
                    sizes=[
                        'sizes2',
                        'sizes3'
                    ],
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        redis=Redis(
            regions=[
                'regions7'
            ],
            versions=[
                'versions7'
            ],
            layouts=[
                Layout(
                    num_nodes=190,
                    sizes=[
                        'sizes2',
                        'sizes3'
                    ],
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    version_availability=VersionAvailability(
        mongodb=[
            Mongodb1(
                end_of_availability='end_of_availability4',
                end_of_life='end_of_life4',
                version='version4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Mongodb1(
                end_of_availability='end_of_availability4',
                end_of_life='end_of_life4',
                version='version4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        mysql=[
            Mongodb1(
                end_of_availability='end_of_availability0',
                end_of_life='end_of_life0',
                version='version0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Mongodb1(
                end_of_availability='end_of_availability0',
                end_of_life='end_of_life0',
                version='version0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        pg=[
            Mongodb1(
                end_of_availability='end_of_availability4',
                end_of_life='end_of_life4',
                version='version4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        redis=[
            Mongodb1(
                end_of_availability='end_of_availability8',
                end_of_life='end_of_life8',
                version='version8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



