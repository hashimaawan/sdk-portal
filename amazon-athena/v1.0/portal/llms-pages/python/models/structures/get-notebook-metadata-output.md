# Get Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldE5vdGVib29rTWV0YWRhdGFPdXRwdXQ

*This model accepts additional fields of type Any.*


# Class Name

`GetNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_metadata` | [`NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/notebook-metadata-1.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.get_notebook_metadata_output import GetNotebookMetadataOutput
from amazonathena.models.notebook_metadata_1 import NotebookMetadata1
from amazonathena.models.notebook_type_1 import NotebookType1

get_notebook_metadata_output = GetNotebookMetadataOutput(
    notebook_metadata=NotebookMetadata1(
        notebook_id='NotebookId0',
        name='Name0',
        work_group='WorkGroup2',
        creation_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        mtype=NotebookType1.IPYNB,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



