# Batch Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRPdXRwdXQ

*This model accepts additional fields of type Any.*


# Class Name

`BatchGetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prepared_statements` | [`List[PreparedStatement]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/prepared-statement.md) | Optional | - |
| `unprocessed_prepared_statement_names` | [`List[UnprocessedPreparedStatementName]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/unprocessed-prepared-statement-name.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.batch_get_prepared_statement_output import BatchGetPreparedStatementOutput
from amazonathena.models.prepared_statement import PreparedStatement
from amazonathena.models.unprocessed_prepared_statement_name import UnprocessedPreparedStatementName

batch_get_prepared_statement_output = BatchGetPreparedStatementOutput(
    prepared_statements=[
        PreparedStatement(
            statement_name='StatementName2',
            query_statement='QueryStatement6',
            work_group_name='WorkGroupName6',
            description='Description2',
            last_modified_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        PreparedStatement(
            statement_name='StatementName2',
            query_statement='QueryStatement6',
            work_group_name='WorkGroupName6',
            description='Description2',
            last_modified_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        PreparedStatement(
            statement_name='StatementName2',
            query_statement='QueryStatement6',
            work_group_name='WorkGroupName6',
            description='Description2',
            last_modified_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    unprocessed_prepared_statement_names=[
        UnprocessedPreparedStatementName(
            statement_name='StatementName0',
            error_code='ErrorCode2',
            error_message='ErrorMessage8',
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



