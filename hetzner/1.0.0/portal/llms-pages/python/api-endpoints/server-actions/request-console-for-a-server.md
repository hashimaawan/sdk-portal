# Request Console for a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRlJlcXVlc3QlMjUyMENvbnNvbGUlMjUyMGZvciUyNTIwYSUyNTIwU2VydmVy

Requests credentials for remote access via VNC over websocket to keyboard, monitor, and mouse for a Server. The provided URL is valid for 1 minute, after this period a new url needs to be created to connect to the Server. How long the connection is open after the initial connect is not subject to this timeout.

:information_source: **Note** This endpoint does not require authentication.

```python
def request_console_for_a_server(self,
                                id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

[`ServersActionsRequestConsoleResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/servers-actions-request-console-response.md)


# Example Usage

```python
id = 112

result = server_actions_controller.request_console_for_a_server(id)
print(result)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "request_console",
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
  "password": "9MQaTg2VAGI0FIpc10k3UpRXcHj2wQ6x",
  "wss_url": "wss://console.hetzner.cloud/?server_id=1&token=3db32d15-af2f-459c-8bf8-dee1fd05f49c"
}
```



