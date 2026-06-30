# Forbidden

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRkZvcmJpZGRlbg

*This model accepts additional fields of type Object.*


# Class Name

`ForbiddenException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/error-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
begin
  # make the API call
rescue ForbiddenException => e
  puts "Caught ForbiddenException: #{e.message}"
end
```



