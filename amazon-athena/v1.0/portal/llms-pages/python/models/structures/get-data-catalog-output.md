# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0

*This model accepts additional fields of type Any.*


# Class Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data_catalog` | [`DataCatalog2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/data-catalog-2.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.data_catalog_2 import DataCatalog2
from amazonathena.models.data_catalog_type_1 import DataCatalogType1
from amazonathena.models.get_data_catalog_output import GetDataCatalogOutput
from amazonathena.models.parameters import Parameters

get_data_catalog_output = GetDataCatalogOutput(
    data_catalog=DataCatalog2(
        name='Name4',
        mtype=DataCatalogType1.GLUE,
        description='Description2',
        parameters=Parameters(
            additional_properties={
                'exampleAdditionalProperty': 'Parameters_additionalProperties2'
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



