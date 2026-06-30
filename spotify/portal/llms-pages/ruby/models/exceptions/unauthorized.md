# Unauthorized

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlVuYXV0aG9yaXplZA

*This model accepts additional fields of type Object.*


# Class Name

`UnauthorizedException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`ErrorObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/error-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
begin
  # make the API call
rescue UnauthorizedException => e
  puts "Caught UnauthorizedException: #{e.message}"
end
```



