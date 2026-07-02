# Batch Get Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`BatchGetPreparedStatementInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prepared_statement_names` | `List[str]` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `work_group` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.batch_get_prepared_statement_input import BatchGetPreparedStatementInput

batch_get_prepared_statement_input = BatchGetPreparedStatementInput(
    prepared_statement_names=[
        'PreparedStatementNames0',
        'PreparedStatementNames1'
    ],
    work_group='WorkGroup8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



