# List Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhSW5wdXQ

*This model accepts additional fields of type Any.*


# Class Name

`ListTableMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `database_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `expression` | `str` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `256` |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.list_table_metadata_input import ListTableMetadataInput

list_table_metadata_input = ListTableMetadataInput(
    catalog_name='CatalogName2',
    database_name='DatabaseName2',
    expression='Expression0',
    next_token='NextToken8',
    max_results=50,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



