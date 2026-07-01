# Servers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `TrueClass \| FalseClass` | Optional | If true, prevents the Server from being deleted (currently delete and rebuild attribute needs to have the same value) |
| `rebuild` | `TrueClass \| FalseClass` | Optional | If true, prevents the Server from being rebuilt (currently delete and rebuild attribute needs to have the same value) |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
servers_actions_change_protection_request = ServersActionsChangeProtectionRequest.new(
  delete: true,
  rebuild: true,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



