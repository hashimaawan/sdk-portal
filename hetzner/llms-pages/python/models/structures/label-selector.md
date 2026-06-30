# Label Selector

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I


# Class Name

`LabelSelector`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selector` | `str` | Required | Label selector |


# Example

```python
from hetznercloudapi.models.label_selector import LabelSelector

label_selector = LabelSelector(
    selector='env=prod'
)
```



