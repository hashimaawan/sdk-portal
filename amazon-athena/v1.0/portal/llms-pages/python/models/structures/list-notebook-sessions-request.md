# List Notebook Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va1Nlc3Npb25zUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`ListNotebookSessionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.list_notebook_sessions_request import ListNotebookSessionsRequest

list_notebook_sessions_request = ListNotebookSessionsRequest(
    notebook_id='NotebookId6',
    max_results=100,
    next_token='NextToken6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



