# Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdA

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Result`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `metric` | `Dict[str, str]` | Required | An object containing the metric labels. |
| `values` | List[List[int \| str]] | Required | This is 2d List of a container for one-of cases. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.result import Result

result = Result(
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
```



