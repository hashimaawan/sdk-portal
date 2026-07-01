# Servers Actions Request Console Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3QlMjUyMENvbnNvbGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsRequestConsoleResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action.md) | Required | - |
| `password` | `String` | Required | VNC password to use for this connection (this password only works in combination with a wss_url with valid token) |
| `wss_url` | `String` | Required | URL of websocket proxy to use; this includes a token which is valid for a limited time only |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
servers_actions_request_console_response = ServersActionsRequestConsoleResponse.new(
  action: Action.new(
    command: 'start_server',
    error: Error.new(
      code: 'action_failed',
      message: 'Action failed',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    finished: '2016-01-30T23:55:00+00:00',
    id: 42,
    progress: 100,
    resources: [
      Resource.new(
        id: 42,
        type: 'server',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    started: '2016-01-30T23:55:00+00:00',
    status: Status::RUNNING,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  password: '9MQaTg2VAGI0FIpc10k3UpRXcHj2wQ6x',
  wss_url: 'wss://console.hetzner.cloud/?server_id=1&token=3db32d15-af2f-459c-8bf8-dee1fd05f49c',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



