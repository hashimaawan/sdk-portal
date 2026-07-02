# Create Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZURhdGFDYXRhbG9nSW5wdXQ

*This model accepts additional fields of type Any.*


# Class Name

`CreateDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `mtype` | [`DataCatalogType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/data-catalog-type-1.md) | Required | - |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/parameters.md) | Optional | - |
| `tags` | [`List[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/tag.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.create_data_catalog_input import CreateDataCatalogInput
from amazonathena.models.data_catalog_type_1 import DataCatalogType1
from amazonathena.models.parameters import Parameters
from amazonathena.models.tag import Tag

create_data_catalog_input = CreateDataCatalogInput(
    name='Name0',
    mtype=DataCatalogType1.LAMBDA,
    description='Description6',
    parameters=Parameters(
        additional_properties={
            'exampleAdditionalProperty': 'Parameters_additionalProperties2'
        }
    ),
    tags=[
        Tag(
            key='Key0',
            value='Value6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



