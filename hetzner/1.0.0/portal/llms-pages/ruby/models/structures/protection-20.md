# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server

*This model accepts additional fields of type Object.*


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `TrueClass \| FalseClass` | Required | If true, prevents the Server from being deleted |
| `rebuild` | `TrueClass \| FalseClass` | Required | If true, prevents the Server from being rebuilt |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
protection20 = Protection20.new(
  delete: false,
  rebuild: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



