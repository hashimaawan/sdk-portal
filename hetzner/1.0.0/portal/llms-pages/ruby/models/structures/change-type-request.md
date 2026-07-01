# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer_type` | `String` | Required | ID or name of Load Balancer type the Load Balancer should migrate to |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
change_type_request = ChangeTypeRequest.new(
  load_balancer_type: 'lb21',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



