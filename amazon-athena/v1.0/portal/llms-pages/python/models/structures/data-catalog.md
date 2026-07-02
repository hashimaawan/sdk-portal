# Data Catalog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9n

<p>Contains information about a data catalog in an Amazon Web Services account.</p> <note> <p>In the Athena console, data catalogs are listed as "data sources" on the <b>Data sources</b> page under the <b>Data source name</b> column.</p> </note>
*This model accepts additional fields of type Any.*


# Class Name

`DataCatalog`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `mtype` | [`DataCatalogType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/data-catalog-type-1.md) | Required | - |
| `parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/parameters.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.data_catalog import DataCatalog
from amazonathena.models.data_catalog_type_1 import DataCatalogType1
from amazonathena.models.parameters import Parameters

data_catalog = DataCatalog(
    name='Name8',
    mtype=DataCatalogType1.LAMBDA,
    description='Description8',
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



