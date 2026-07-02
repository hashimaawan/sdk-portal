# List Prepared Statements Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RQcmVwYXJlZFN0YXRlbWVudHNPdXRwdXQ

*This model accepts additional fields of type Any.*


# Class Name

`ListPreparedStatementsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prepared_statements` | [`List[PreparedStatementSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/prepared-statement-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.list_prepared_statements_output import ListPreparedStatementsOutput
from amazonathena.models.prepared_statement_summary import PreparedStatementSummary

list_prepared_statements_output = ListPreparedStatementsOutput(
    prepared_statements=[
        PreparedStatementSummary(
            statement_name='StatementName2',
            last_modified_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    next_token='NextToken2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



