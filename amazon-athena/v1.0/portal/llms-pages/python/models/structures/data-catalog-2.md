# Data Catalog 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nMg


# Class Name

`DataCatalog2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `mtype` | [`DataCatalogType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/data-catalog-type-1.md) | Required | - |
| `parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/parameters.md) | Optional | - |


# Example

```python
from amazonathena.models.data_catalog_2 import DataCatalog2
from amazonathena.models.data_catalog_type_1_enum import DataCatalogType1Enum
from amazonathena.models.parameters import Parameters

data_catalog_2 = DataCatalog2(
    name='Name2',
    mtype=DataCatalogType1Enum.HIVE,
    description='Description4',
    parameters=Parameters()
)
```



