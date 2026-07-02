# Update Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZVByZXBhcmVkU3RhdGVtZW50SW5wdXQ

*This model accepts additional fields of type Any.*


# Class Name

`UpdatePreparedStatementInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statement_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `work_group` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `query_statement` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.update_prepared_statement_input import UpdatePreparedStatementInput

update_prepared_statement_input = UpdatePreparedStatementInput(
    statement_name='StatementName6',
    work_group='WorkGroup0',
    query_statement='QueryStatement0',
    description='Description8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



