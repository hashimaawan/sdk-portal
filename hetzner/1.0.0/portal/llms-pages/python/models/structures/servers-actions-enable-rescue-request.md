# Servers Actions Enable Rescue Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXF1ZXN0


# Class Name

`ServersActionsEnableRescueRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ssh_keys` | `List[int]` | Optional | Array of SSH key IDs which should be injected into the rescue system. |
| `mtype` | [`Type65Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-65.md) | Optional | Type of rescue system to boot (default: `linux64`) |


# Example

```python
from hetznercloudapi.models.servers_actions_enable_rescue_request import ServersActionsEnableRescueRequest
from hetznercloudapi.models.type_65_enum import Type65Enum

servers_actions_enable_rescue_request = ServersActionsEnableRescueRequest(
    ssh_keys=[
        2323
    ],
    mtype=Type65Enum.LINUX64
)
```



