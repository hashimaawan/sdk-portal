# Too Many Requests

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlRvb01hbnlSZXF1ZXN0cw

*This model accepts additional fields of type Object.*


# Class Name

`TooManyRequestsException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/error-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
begin
  # make the API call
rescue TooManyRequestsException => e
  puts "Caught TooManyRequestsException: #{e.message}"
end
```



