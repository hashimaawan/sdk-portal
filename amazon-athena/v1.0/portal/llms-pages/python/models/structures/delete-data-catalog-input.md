# Delete Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRlbGV0ZURhdGFDYXRhbG9nSW5wdXQ

*This model accepts additional fields of type Any.*


# Class Name

`DeleteDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.delete_data_catalog_input import DeleteDataCatalogInput

delete_data_catalog_input = DeleteDataCatalogInput(
    name='Name2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



