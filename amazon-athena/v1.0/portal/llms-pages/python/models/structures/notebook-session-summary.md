# Notebook Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRk5vdGVib29rU2Vzc2lvblN1bW1hcnk

Contains the notebook session ID and notebook session creation time.


# Class Name

`NotebookSessionSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `creation_time` | `datetime` | Optional | - |


# Example

```python
import dateutil.parser

from amazonathena.models.notebook_session_summary import NotebookSessionSummary

notebook_session_summary = NotebookSessionSummary(
    session_id='SessionId2',
    creation_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z')
)
```



