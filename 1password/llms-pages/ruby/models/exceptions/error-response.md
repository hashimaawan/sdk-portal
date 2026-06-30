# Error Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRkVycm9yUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`ErrorResponseException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `String` | Optional | A message detailing the error |
| `status` | `Integer` | Optional | HTTP Status Code |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
begin
  # make the API call
rescue ErrorResponseException => e
  puts "Caught ErrorResponseException: #{e.message}"
end
```



