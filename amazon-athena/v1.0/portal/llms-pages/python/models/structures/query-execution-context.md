# Query Execution Context

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dA

The database and data catalog context in which the query execution occurs.

*This model accepts additional fields of type Any.*


# Class Name

`QueryExecutionContext`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `catalog` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.query_execution_context import QueryExecutionContext

query_execution_context = QueryExecutionContext(
    database='Database4',
    catalog='Catalog0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



