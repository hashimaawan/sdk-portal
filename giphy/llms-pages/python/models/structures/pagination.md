# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/python/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions.


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `count` | `int` | Optional | Total number of items returned. |
| `offset` | `int` | Optional | Position in pagination. |
| `total_count` | `int` | Optional | Total number of items available. |


# Example

```python
from giphyapi.models.pagination import Pagination

pagination = Pagination(
    count=25,
    offset=75,
    total_count=250
)
```



