# Data

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Data`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `result` | [`List[Result]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/result.md) | Required | Result of query. |
| `result_type` | `str` | Required, Constant | **Value**: `"matrix"` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.data import Data
from digitaloceanapi.models.result import Result

data = Data(
    result=[
        Result(
            metric={
                'host_id': '19201920'
            },
            values=[
                [
                    1435781430,
                    '1'
                ],
                [
                    1435781445,
                    '1'
                ]
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



