# List Databases Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`ListDatabasesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.list_databases_input import ListDatabasesInput

list_databases_input = ListDatabasesInput(
    catalog_name='CatalogName0',
    next_token='NextToken6',
    max_results=2,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



