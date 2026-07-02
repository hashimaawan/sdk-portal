# Get Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXF1ZXN0


# Class Name

`GetSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |


# Example

```python
from amazonathena.models.get_session_request import GetSessionRequest

get_session_request = GetSessionRequest(
    session_id='SessionId4'
)
```



