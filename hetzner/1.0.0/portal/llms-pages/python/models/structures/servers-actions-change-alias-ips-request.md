# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alias_ips` | `List[str]` | Required | New alias IPs to set for this Server |
| `network` | `int` | Required | ID of an existing Network already attached to the Server |


# Example

```python
from hetznercloudapi.models.servers_actions_change_alias_ips_request import ServersActionsChangeAliasIpsRequest

servers_actions_change_alias_ips_request = ServersActionsChangeAliasIpsRequest(
    alias_ips=[
        '10.0.1.2'
    ],
    network=4711
)
```



