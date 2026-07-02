# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ

*This model accepts additional fields of type Any.*


# Class Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query` | [`NamedQuery1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/named-query-1.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.get_named_query_output import GetNamedQueryOutput
from amazonathena.models.named_query_1 import NamedQuery1

get_named_query_output = GetNamedQueryOutput(
    named_query=NamedQuery1(
        name='Name0',
        database='Database8',
        query_string='QueryString2',
        description='Description6',
        named_query_id='NamedQueryId2',
        work_group='WorkGroup2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



