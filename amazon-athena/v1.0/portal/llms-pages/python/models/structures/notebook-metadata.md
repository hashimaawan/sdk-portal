# Notebook Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRk5vdGVib29rTWV0YWRhdGE

Contains metadata for notebook, including the notebook name, ID, workgroup, and time created.

*This model accepts additional fields of type Any.*


# Class Name

`NotebookMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `name` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `work_group` | `str` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `creation_time` | `datetime` | Optional | - |
| `mtype` | [`NotebookType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/notebook-type-1.md) | Optional | - |
| `last_modified_time` | `datetime` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.notebook_metadata import NotebookMetadata
from amazonathena.models.notebook_type_1 import NotebookType1

notebook_metadata = NotebookMetadata(
    notebook_id='NotebookId4',
    name='Name4',
    work_group='WorkGroup6',
    creation_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    mtype=NotebookType1.IPYNB,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



