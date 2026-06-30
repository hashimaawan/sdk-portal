# Track 1

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlRyYWNrMQ

*This model accepts additional fields of type Object.*


# Class Name

`Track1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `uri` | `String` | Optional | Spotify URI |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
track1 = Track1.new(
  uri: 'uri0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



