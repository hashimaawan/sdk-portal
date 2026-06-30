# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkVycm9y

Error message for the Action if error occurred, otherwise null


# Class Name

`Error`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | `str` | Required | Fixed machine readable code |
| `message` | `str` | Required | Humanized error message |


# Example

```python
from hetznercloudapi.models.error import Error

error = Error(
    code='action_failed',
    message='Action failed'
)
```



