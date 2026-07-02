# Get Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`GetTableMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `database_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `table_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.get_table_metadata_input import GetTableMetadataInput

get_table_metadata_input = GetTableMetadataInput(
    catalog_name='CatalogName4',
    database_name='DatabaseName4',
    table_name='TableName6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



