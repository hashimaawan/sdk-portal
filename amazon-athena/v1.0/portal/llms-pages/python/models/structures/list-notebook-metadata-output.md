# List Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhT3V0cHV0

*This model accepts additional fields of type Any.*


# Class Name

`ListNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `notebook_metadata_list` | [`List[NotebookMetadata]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/notebook-metadata.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.list_notebook_metadata_output import ListNotebookMetadataOutput
from amazonathena.models.notebook_metadata import NotebookMetadata
from amazonathena.models.notebook_type_1 import NotebookType1

list_notebook_metadata_output = ListNotebookMetadataOutput(
    next_token='NextToken8',
    notebook_metadata_list=[
        NotebookMetadata(
            notebook_id='NotebookId4',
            name='Name4',
            work_group='WorkGroup6',
            creation_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            mtype=NotebookType1.IPYNB,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



