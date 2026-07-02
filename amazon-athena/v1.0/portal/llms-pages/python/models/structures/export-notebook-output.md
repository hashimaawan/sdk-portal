# Export Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkV4cG9ydE5vdGVib29rT3V0cHV0

*This model accepts additional fields of type Any.*


# Class Name

`ExportNotebookOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_metadata` | [`NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/notebook-metadata-1.md) | Optional | - |
| `payload` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.export_notebook_output import ExportNotebookOutput
from amazonathena.models.notebook_metadata_1 import NotebookMetadata1
from amazonathena.models.notebook_type_1 import NotebookType1

export_notebook_output = ExportNotebookOutput(
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
    payload='Payload6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



