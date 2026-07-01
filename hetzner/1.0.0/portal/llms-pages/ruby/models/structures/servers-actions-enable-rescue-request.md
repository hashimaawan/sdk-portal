# Servers Actions Enable Rescue Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsEnableRescueRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ssh_keys` | `Array[Integer]` | Optional | Array of SSH key IDs which should be injected into the rescue system. |
| `type` | [`Type65`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-65.md) | Optional | Type of rescue system to boot (default: `linux64`) |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
servers_actions_enable_rescue_request = ServersActionsEnableRescueRequest.new(
  ssh_keys: [
    2323
  ],
  type: Type65::LINUX64,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



