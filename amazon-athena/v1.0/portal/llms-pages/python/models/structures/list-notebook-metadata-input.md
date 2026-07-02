# List Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhSW5wdXQ

*This model accepts additional fields of type Any.*


# Class Name

`ListNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filters` | [`Filters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/filters.md) | Optional | - |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `work_group` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.filters import Filters
from amazonathena.models.list_notebook_metadata_input import ListNotebookMetadataInput

list_notebook_metadata_input = ListNotebookMetadataInput(
    work_group='WorkGroup6',
    filters=Filters(
        name='Name2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    next_token='NextToken4',
    max_results=50,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



