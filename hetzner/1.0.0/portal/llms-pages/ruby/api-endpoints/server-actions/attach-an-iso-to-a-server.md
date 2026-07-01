# Attach an ISO to a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkF0dGFjaCUyNTIwYW4lMjUyMElTTyUyNTIwdG8lMjUyMGElMjUyMFNlcnZlcg

Attaches an ISO to a Server. The Server will immediately see it as a new disk. An already attached ISO will automatically be detached before the new ISO is attached.

Servers with attached ISOs have a modified boot order: They will try to boot from the ISO first before falling back to hard disk.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def attach_an_iso_to_a_server(id,
                              body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Server |
| `body` | [`ServersActionsAttachIsoRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/servers-actions-attach-iso-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action-response.md)


# Example Usage

```ruby
id = 112

body = ServersActionsAttachIsoRequest.new(
  'FreeBSD-11.0-RELEASE-amd64-dvd1'
)

result = server_actions_controller.attach_an_iso_to_a_server(
  id,
  body: body
)
puts result
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "attach_iso",
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



