# Get Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldE5vdGVib29rTWV0YWRhdGFJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`GetNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.get_notebook_metadata_input import GetNotebookMetadataInput

get_notebook_metadata_input = GetNotebookMetadataInput(
    notebook_id='NotebookId4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



