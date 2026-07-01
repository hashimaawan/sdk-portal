# Change Protection Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0MQ

*This model accepts additional fields of type Object.*


# Class Name

`ChangeProtectionRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `TrueClass \| FalseClass` | Optional | If true, prevents the Network from being deleted |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
change_protection_request1 = ChangeProtectionRequest1.new(
  delete: true,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



