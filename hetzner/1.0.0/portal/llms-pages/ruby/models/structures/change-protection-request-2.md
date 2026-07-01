# Change Protection Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0Mg

*This model accepts additional fields of type Object.*


# Class Name

`ChangeProtectionRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `TrueClass \| FalseClass` | Optional | If true, prevents the Primary IP from being deleted |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
change_protection_request2 = ChangeProtectionRequest2.new(
  delete: true,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



