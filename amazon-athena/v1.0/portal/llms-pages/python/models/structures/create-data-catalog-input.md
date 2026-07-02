# Create Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZURhdGFDYXRhbG9nSW5wdXQ


# Class Name

`CreateDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `mtype` | [`DataCatalogType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/data-catalog-type-1.md) | Required | - |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/parameters.md) | Optional | - |
| `tags` | [`List[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/tag.md) | Optional | - |


# Example

```python
from amazonathena.models.create_data_catalog_input import CreateDataCatalogInput
from amazonathena.models.data_catalog_type_1_enum import DataCatalogType1Enum
from amazonathena.models.parameters import Parameters
from amazonathena.models.tag import Tag

create_data_catalog_input = CreateDataCatalogInput(
    name='Name0',
    mtype=DataCatalogType1Enum.LAMBDA,
    description='Description6',
    parameters=Parameters(),
    tags=[
        Tag(
            key='Key0',
            value='Value6'
        )
    ]
)
```



