# Get Database Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldERhdGFiYXNlSW5wdXQ

*This model accepts additional fields of type Any.*


# Class Name

`GetDatabaseInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `database_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.get_database_input import GetDatabaseInput

get_database_input = GetDatabaseInput(
    catalog_name='CatalogName4',
    database_name='DatabaseName4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



