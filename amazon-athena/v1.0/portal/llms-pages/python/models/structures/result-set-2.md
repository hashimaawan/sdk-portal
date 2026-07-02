# Result Set 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdFNldDI

*This model accepts additional fields of type Any.*


# Class Name

`ResultSet2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rows` | [`List[Row]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/row.md) | Optional | - |
| `result_set_metadata` | [`ResultSetMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/result-set-metadata-2.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.column_info import ColumnInfo
from amazonathena.models.datum import Datum
from amazonathena.models.result_set_2 import ResultSet2
from amazonathena.models.result_set_metadata_2 import ResultSetMetadata2
from amazonathena.models.row import Row

result_set_2 = ResultSet2(
    rows=[
        Row(
            data=[
                Datum(
                    var_char_value='VarCharValue8',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                Datum(
                    var_char_value='VarCharValue8',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Row(
            data=[
                Datum(
                    var_char_value='VarCharValue8',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                Datum(
                    var_char_value='VarCharValue8',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    result_set_metadata=ResultSetMetadata2(
        column_info=[
            ColumnInfo(
                name='Name6',
                mtype='Type6',
                catalog_name='CatalogName0',
                schema_name='SchemaName0',
                table_name='TableName2',
                label='Label4',
                precision=48,
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



