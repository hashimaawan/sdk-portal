# Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFByZXBhcmVkU3RhdGVtZW50T3V0cHV0


# Class Name

`GetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prepared_statement` | [`PreparedStatement1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/prepared-statement-1.md) | Optional | - |


# Example

```python
import dateutil.parser

from amazonathena.models.get_prepared_statement_output import GetPreparedStatementOutput
from amazonathena.models.prepared_statement_1 import PreparedStatement1

get_prepared_statement_output = GetPreparedStatementOutput(
    prepared_statement=PreparedStatement1(
        statement_name='StatementName4',
        query_statement='QueryStatement8',
        work_group_name='WorkGroupName8',
        description='Description0',
        last_modified_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z')
    )
)
```



