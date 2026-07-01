# Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByb3RlY3Rpb24

Protection configuration for the Resource

*This model accepts additional fields of type Object.*


# Class Name

`Protection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `TrueClass \| FalseClass` | Required | If true, prevents the Resource from being deleted |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
protection = Protection.new(
  delete: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



