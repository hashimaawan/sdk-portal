# Servers Actions Request Console Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3QlMjUyMENvbnNvbGUlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsRequestConsoleResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/action.md) | Required | - |
| `password` | `String` | Required | VNC password to use for this connection (this password only works in combination with a wss_url with valid token) |
| `wss_url` | `String` | Required | URL of websocket proxy to use; this includes a token which is valid for a limited time only |


# Example

```ruby
servers_actions_request_console_response = ServersActionsRequestConsoleResponse.new(
  Action.new(
    'start_server',
    Error.new(
      'action_failed',
      'Action failed'
    ),
    '2016-01-30T23:55:00+00:00',
    42,
    100,
    [
      Resource.new(
        42,
        'server'
      )
    ],
    '2016-01-30T23:55:00+00:00',
    StatusEnum::RUNNING
  ),
  '9MQaTg2VAGI0FIpc10k3UpRXcHj2wQ6x',
  'wss://console.hetzner.cloud/?server_id=1&token=3db32d15-af2f-459c-8bf8-dee1fd05f49c'
)
```



