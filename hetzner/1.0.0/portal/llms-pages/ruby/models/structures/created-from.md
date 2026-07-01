# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from

*This model accepts additional fields of type Object.*


# Class Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Required | ID of the Server the Image was created from |
| `name` | `String` | Required | Server name at the time the Image was created |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
created_from = CreatedFrom.new(
  id: 1,
  name: 'Server',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



