# Create Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZU5vdGVib29rT3V0cHV0

*This model accepts additional fields of type Any.*


# Class Name

`CreateNotebookOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.create_notebook_output import CreateNotebookOutput

create_notebook_output = CreateNotebookOutput(
    notebook_id='NotebookId6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



