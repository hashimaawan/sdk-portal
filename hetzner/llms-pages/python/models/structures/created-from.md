# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from


# Class Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Required | ID of the Server the Image was created from |
| `name` | `str` | Required | Server name at the time the Image was created |


# Example

```python
from hetznercloudapi.models.created_from import CreatedFrom

created_from = CreatedFrom(
    id=1,
    name='Server'
)
```



