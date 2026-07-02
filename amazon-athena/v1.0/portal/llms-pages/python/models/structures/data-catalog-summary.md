# Data Catalog Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nU3VtbWFyeQ

The summary information for the data catalog, which includes its name and type.

*This model accepts additional fields of type Any.*


# Class Name

`DataCatalogSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `mtype` | [`DataCatalogType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/data-catalog-type-2.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.data_catalog_summary import DataCatalogSummary
from amazonathena.models.data_catalog_type_2 import DataCatalogType2

data_catalog_summary = DataCatalogSummary(
    catalog_name='CatalogName4',
    mtype=DataCatalogType2.HIVE,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



