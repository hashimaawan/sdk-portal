# Enable Rescue Mode for a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkVuYWJsZSUyNTIwUmVzY3VlJTI1MjBNb2RlJTI1MjBmb3IlMjUyMGElMjUyMFNlcnZlcg

Enable the Hetzner Rescue System for this Server. The next time a Server with enabled rescue mode boots it will start a special minimal Linux distribution designed for repair and reinstall.

In case a Server cannot boot on its own you can use this to access a Server’s disks.

Rescue Mode is automatically disabled when you first boot into it or if you do not use it for 60 minutes.

Enabling rescue mode will not [reboot](https://docs.hetzner.cloud/#server-actions-soft-reboot-a-server) your Server — you will have to do this yourself.

:information_source: **Note** This endpoint does not require authentication.

```python
def enable_rescue_mode_for_a_server(self,
                                   id,
                                   body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`ServersActionsEnableRescueRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/servers-actions-enable-rescue-request.md) | Body, Optional | - |


# Response Type

**201**: The `root_password` key in the reply contains the root password that can be used to access the booted rescue system.

The `action` key in the reply contains an Action object with this structure

[`ServersActionsEnableRescueResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/servers-actions-enable-rescue-response.md)


# Example Usage

```python
id = 112

body = ServersActionsEnableRescueRequest(
    ssh_keys=[
        2323
    ]
)

result = server_actions_controller.enable_rescue_mode_for_a_server(
    id,
    body=body
)
print(result)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "enable_rescue",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": "2016-01-30T23:56:00+00:00",
    "id": 13,
    "progress": 100,
    "resources": [
      {
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  },
  "root_password": "zCWbFhnu950dUTko5f40"
}
```



