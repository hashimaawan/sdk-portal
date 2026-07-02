# Query Execution Context 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dDE

*This model accepts additional fields of type Any.*


# Class Name

`QueryExecutionContext1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `catalog` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.query_execution_context_1 import QueryExecutionContext1

query_execution_context_1 = QueryExecutionContext1(
    database='Database6',
    catalog='Catalog2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



