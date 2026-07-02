# Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFByZXBhcmVkU3RhdGVtZW50T3V0cHV0

*This model accepts additional fields of type Any.*


# Class Name

`GetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prepared_statement` | [`PreparedStatement1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/prepared-statement-1.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.get_prepared_statement_output import GetPreparedStatementOutput
from amazonathena.models.prepared_statement_1 import PreparedStatement1

get_prepared_statement_output = GetPreparedStatementOutput(
    prepared_statement=PreparedStatement1(
        statement_name='StatementName4',
        query_statement='QueryStatement8',
        work_group_name='WorkGroupName8',
        description='Description0',
        last_modified_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



