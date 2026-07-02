# Update Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZU5vdGVib29rTWV0YWRhdGFJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`UpdateNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `client_request_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.update_notebook_metadata_input import UpdateNotebookMetadataInput

update_notebook_metadata_input = UpdateNotebookMetadataInput(
    notebook_id='NotebookId0',
    name='Name0',
    client_request_token='ClientRequestToken4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



