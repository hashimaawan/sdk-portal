# Import Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkltcG9ydE5vdGVib29rSW5wdXQ

*This model accepts additional fields of type Any.*


# Class Name

`ImportNotebookInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `payload` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |
| `mtype` | [`NotebookType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/notebook-type-2.md) | Required | - |
| `client_request_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.import_notebook_input import ImportNotebookInput
from amazonathena.models.notebook_type_2 import NotebookType2

import_notebook_input = ImportNotebookInput(
    work_group='WorkGroup8',
    name='Name6',
    payload='Payload2',
    mtype=NotebookType2.IPYNB,
    client_request_token='ClientRequestToken0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



