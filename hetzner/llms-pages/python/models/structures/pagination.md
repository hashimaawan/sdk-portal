# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlBhZ2luYXRpb24


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `last_page` | `float` | Required | ID of the last page available. Can be null if the current page is the last one. |
| `next_page` | `float` | Required | ID of the next page. Can be null if the current page is the last one. |
| `page` | `float` | Required | Current page number |
| `per_page` | `float` | Required | Maximum number of items shown per page in the response |
| `previous_page` | `float` | Required | ID of the previous page. Can be null if the current page is the first one. |
| `total_entries` | `float` | Required | The total number of entries that exist in the database for this query. Nullable if unknown. |


# Example

```python
from hetznercloudapi.models.pagination import Pagination

pagination = Pagination(
    last_page=4,
    next_page=4,
    page=3,
    per_page=25,
    previous_page=2,
    total_entries=100
)
```



