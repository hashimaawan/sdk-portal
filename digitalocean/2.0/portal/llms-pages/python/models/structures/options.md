# Options

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRk9wdGlvbnM

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Options`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mongodb` | [`Mongodb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/mongodb.md) | Optional | - |
| `mysql` | [`Mysql`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/mysql.md) | Optional | - |
| `pg` | [`Pg`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/pg.md) | Optional | - |
| `redis` | [`Redis`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/redis.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.layout import Layout
from digitaloceanapi.models.mongodb import Mongodb
from digitaloceanapi.models.mysql import Mysql
from digitaloceanapi.models.options import Options
from digitaloceanapi.models.pg import Pg
from digitaloceanapi.models.redis import Redis

options = Options(
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
)
```



