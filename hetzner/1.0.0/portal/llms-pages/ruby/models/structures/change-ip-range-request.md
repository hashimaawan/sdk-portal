# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ChangeIpRangeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip_range` | `String` | Required | The new prefix for the whole Network |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
change_ip_range_request = ChangeIpRangeRequest.new(
  ip_range: '10.0.0.0/12',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



