# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRk1ldGE


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/pagination.md) | Required | - |


# Example

```python
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.pagination import Pagination

meta = Meta(
    pagination=Pagination(
        last_page=4,
        next_page=4,
        page=3,
        per_page=25,
        previous_page=2,
        total_entries=100
    )
)
```



