# Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0


# Class Name

`ChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Optional | If true, prevents the Floating IP from being deleted |


# Example

```python
from hetznercloudapi.models.change_protection_request import ChangeProtectionRequest

change_protection_request = ChangeProtectionRequest(
    delete=True
)
```



