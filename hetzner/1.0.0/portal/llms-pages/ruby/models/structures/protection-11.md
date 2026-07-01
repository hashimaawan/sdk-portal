# Protection 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByb3RlY3Rpb24xMQ

Protection configuration for the Network

*This model accepts additional fields of type Object.*


# Class Name

`Protection11`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `TrueClass \| FalseClass` | Required | If true, prevents the Network from being deleted |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
protection11 = Protection11.new(
  delete: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



