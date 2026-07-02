# Update Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZURhdGFDYXRhbG9nSW5wdXQ

*This model accepts additional fields of type Any.*


# Class Name

`UpdateDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `mtype` | [`DataCatalogType3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/data-catalog-type-3.md) | Required | - |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/parameters.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.data_catalog_type_3 import DataCatalogType3
from amazonathena.models.parameters import Parameters
from amazonathena.models.update_data_catalog_input import UpdateDataCatalogInput

update_data_catalog_input = UpdateDataCatalogInput(
    name='Name0',
    mtype=DataCatalogType3.HIVE,
    description='Description6',
    parameters=Parameters(
        additional_properties={
            'exampleAdditionalProperty': 'Parameters_additionalProperties2'
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



