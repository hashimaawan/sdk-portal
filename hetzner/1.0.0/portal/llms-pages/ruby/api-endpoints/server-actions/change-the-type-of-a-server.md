# Change the Type of a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkNoYW5nZSUyNTIwdGhlJTI1MjBUeXBlJTI1MjBvZiUyNTIwYSUyNTIwU2VydmVy

Changes the type (Cores, RAM and disk sizes) of a Server.

Server must be powered off for this command to succeed.

This copies the content of its disk, and starts it again.

You can only migrate to Server types with the same `storage_type` and equal or bigger disks. Shrinking disks is not possible as it might destroy data.

If the disk gets upgraded, the Server type can not be downgraded any more. If you plan to downgrade the Server type, set `upgrade_disk` to `false`.

#### Call specific error codes

| Code                          | Description                                                          |
|-------------------------------|----------------------------------------------------------------------|
| `invalid_server_type`         | The server type does not fit for the given server or is deprecated   |
| `server_not_stopped`          | The action requires a stopped server                                 |

:information_source: **Note** This endpoint does not require authentication.

```ruby
def change_the_type_of_a_server(id,
                                body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Server |
| `body` | [`ServersActionsChangeTypeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/servers-actions-change-type-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action-response.md)


# Example Usage

```ruby
id = 112

body = ServersActionsChangeTypeRequest.new(
  'cx11',
  true
)

result = server_actions_controller.change_the_type_of_a_server(
  id,
  body: body
)
puts result
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "change_server_type",
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



