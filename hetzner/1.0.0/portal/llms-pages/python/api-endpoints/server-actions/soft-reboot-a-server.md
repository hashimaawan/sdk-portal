# Soft-Reboot a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRlNvZnQtcmVib290JTI1MjBhJTI1MjBTZXJ2ZXI

Reboots a Server gracefully by sending an ACPI request. The Server operating system must support ACPI and react to the request, otherwise the Server will not reboot.

:information_source: **Note** This endpoint does not require authentication.

```python
def soft_reboot_a_server(self,
                        id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md)


# Example Usage

```python
id = 112

result = server_actions_controller.soft_reboot_a_server(id)
print(result)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "reboot_server",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



