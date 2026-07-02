# List Notebook Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va1Nlc3Npb25zUmVzcG9uc2U

*This model accepts additional fields of type Any.*


# Class Name

`ListNotebookSessionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_sessions_list` | [`List[NotebookSessionSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/notebook-session-summary.md) | Required | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.list_notebook_sessions_response import ListNotebookSessionsResponse
from amazonathena.models.notebook_session_summary import NotebookSessionSummary

list_notebook_sessions_response = ListNotebookSessionsResponse(
    notebook_sessions_list=[
        NotebookSessionSummary(
            session_id='SessionId4',
            creation_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    next_token='NextToken8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



