# Query Execution Context 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dDE


# Class Name

`QueryExecutionContext1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `catalog` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |


# Example

```python
from amazonathena.models.query_execution_context_1 import QueryExecutionContext1

query_execution_context_1 = QueryExecutionContext1(
    database='Database6',
    catalog='Catalog2'
)
```



