# Get Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFJbnB1dA


# Class Name

`GetTableMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `database_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `table_name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```python
from amazonathena.models.get_table_metadata_input import GetTableMetadataInput

get_table_metadata_input = GetTableMetadataInput(
    catalog_name='CatalogName4',
    database_name='DatabaseName4',
    table_name='TableName6'
)
```



