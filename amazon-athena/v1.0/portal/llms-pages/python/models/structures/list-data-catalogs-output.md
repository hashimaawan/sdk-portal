# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ


# Class Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data_catalogs_summary` | [`List[DataCatalogSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/data-catalog-summary.md) | Optional | - |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```python
from amazonathena.models.data_catalog_summary import DataCatalogSummary
from amazonathena.models.data_catalog_type_2_enum import DataCatalogType2Enum
from amazonathena.models.list_data_catalogs_output import ListDataCatalogsOutput

list_data_catalogs_output = ListDataCatalogsOutput(
    data_catalogs_summary=[
        DataCatalogSummary(
            catalog_name='CatalogName4',
            mtype=DataCatalogType2Enum.HIVE
        ),
        DataCatalogSummary(
            catalog_name='CatalogName4',
            mtype=DataCatalogType2Enum.HIVE
        ),
        DataCatalogSummary(
            catalog_name='CatalogName4',
            mtype=DataCatalogType2Enum.HIVE
        )
    ],
    next_token='NextToken2'
)
```



