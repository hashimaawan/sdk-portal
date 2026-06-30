# Reset Root Password of a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRlJlc2V0JTI1MjByb290JTI1MjBQYXNzd29yZCUyNTIwb2YlMjUyMGElMjUyMFNlcnZlcg

Resets the root password. Only works for Linux systems that are running the qemu guest agent. Server must be powered on (status `running`) in order for this operation to succeed.

This will generate a new password for this Server and return it.

If this does not succeed you can use the rescue system to netboot the Server and manually change your Server password by hand.

:information_source: **Note** This endpoint does not require authentication.

```python
def reset_root_password_of_a_server(self,
                                   id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |


# Response Type

**201**: The `root_password` key in the reply contains the new root password that will be active if the Action succeeds.

The `action` key in the reply contains an Action object with this structure:

[`ServersActionsResetPasswordResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/servers-actions-reset-password-response.md)


# Example Usage

```python
id = 112

result = server_actions_controller.reset_root_password_of_a_server(id)
print(result)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "reset_password",
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
  },
  "root_password": "zCWbFhnu950dUTko5f40"
}
```



