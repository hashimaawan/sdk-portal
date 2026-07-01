# Firewall 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZpcmV3YWxsNA

*This model accepts additional fields of type Object.*


# Class Name

`Firewall4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewall` | `Integer` | Optional | ID of the Firewall |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
firewall4 = Firewall4.new(
  firewall: 176,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



