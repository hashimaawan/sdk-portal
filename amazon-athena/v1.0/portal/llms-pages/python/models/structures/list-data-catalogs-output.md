# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ

*This model accepts additional fields of type Any.*


# Class Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data_catalogs_summary` | [`List[DataCatalogSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/data-catalog-summary.md) | Optional | - |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.data_catalog_summary import DataCatalogSummary
from amazonathena.models.data_catalog_type_2 import DataCatalogType2
from amazonathena.models.list_data_catalogs_output import ListDataCatalogsOutput

list_data_catalogs_output = ListDataCatalogsOutput(
    data_catalogs_summary=[
        DataCatalogSummary(
            catalog_name='CatalogName4',
            mtype=DataCatalogType2.HIVE,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        DataCatalogSummary(
            catalog_name='CatalogName4',
            mtype=DataCatalogType2.HIVE,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        DataCatalogSummary(
            catalog_name='CatalogName4',
            mtype=DataCatalogType2.HIVE,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    next_token='NextToken2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



