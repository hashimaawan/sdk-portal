# Table Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlRhYmxlTWV0YWRhdGEy

*This model accepts additional fields of type Any.*


# Class Name

`TableMetadata2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `create_time` | `datetime` | Optional | - |
| `last_access_time` | `datetime` | Optional | - |
| `table_type` | `str` | Optional | **Constraints**: *Maximum Length*: `255` |
| `columns` | [`List[Column]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/column.md) | Optional | - |
| `partition_keys` | [`List[Column]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/column.md) | Optional | - |
| `parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/parameters.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.column import Column
from amazonathena.models.table_metadata_2 import TableMetadata2

table_metadata_2 = TableMetadata2(
    name='Name8',
    create_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    last_access_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    table_type='TableType2',
    columns=[
        Column(
            name='Name0',
            mtype='Type0',
            comment='Comment4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    partition_keys=[
        Column(
            name='Name6',
            mtype='Type6',
            comment='Comment0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Column(
            name='Name6',
            mtype='Type6',
            comment='Comment0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Column(
            name='Name6',
            mtype='Type6',
            comment='Comment0',
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



