# Attach Volume to a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlZvbHVtZSUyNTIwQWN0aW9ucyUyRkF0dGFjaCUyNTIwVm9sdW1lJTI1MjB0byUyNTIwYSUyNTIwU2VydmVy

Attaches a Volume to a Server. Works only if the Server is in the same Location as the Volume.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def attach_volume_to_a_server(id,
                              body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Volume |
| `body` | [`AttachVolumeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/attach-volume-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `attach_volume` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action-response.md)


# Example Usage

```ruby
id = 112

body = AttachVolumeRequest.new(
  43,
  false
)

result = volume_actions_controller.attach_volume_to_a_server(
  id,
  body: body
)
puts result
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "attach_volume",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 43,
        "type": "server"
      },
      {
        "id": 554,
        "type": "volume"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



