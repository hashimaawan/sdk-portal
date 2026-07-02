# Data Catalog Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nU3VtbWFyeQ

The summary information for the data catalog, which includes its name and type.


# Class Name

`DataCatalogSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `mtype` | [`DataCatalogType2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/data-catalog-type-2.md) | Optional | - |


# Example

```python
from amazonathena.models.data_catalog_summary import DataCatalogSummary
from amazonathena.models.data_catalog_type_2_enum import DataCatalogType2Enum

data_catalog_summary = DataCatalogSummary(
    catalog_name='CatalogName4',
    mtype=DataCatalogType2Enum.HIVE
)
```



