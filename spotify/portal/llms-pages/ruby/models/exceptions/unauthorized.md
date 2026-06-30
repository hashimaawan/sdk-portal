# Unauthorized

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlVuYXV0aG9yaXplZA

*This model accepts additional fields of type Object.*


# Class Name

`UnauthorizedException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/error-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
begin
  # make the API call
rescue UnauthorizedException => e
  puts "Caught UnauthorizedException: #{e.message}"
end
```



