# Servers Actions Enable Rescue Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXF1ZXN0


# Class Name

`ServersActionsEnableRescueRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ssh_keys` | `Array[Integer]` | Optional | Array of SSH key IDs which should be injected into the rescue system. |
| `type` | [`Type65Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-65.md) | Optional | Type of rescue system to boot (default: `linux64`) |


# Example

```ruby
servers_actions_enable_rescue_request = ServersActionsEnableRescueRequest.new(
  [
    2323
  ],
  Type65Enum::LINUX64
)
```



