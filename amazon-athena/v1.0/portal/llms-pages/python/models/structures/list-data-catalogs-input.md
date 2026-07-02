# List Data Catalogs Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`ListDataCatalogsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `int` | Optional | **Constraints**: `>= 2`, `<= 50` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.list_data_catalogs_input import ListDataCatalogsInput

list_data_catalogs_input = ListDataCatalogsInput(
    next_token='NextToken4',
    max_results=50,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



