# V2 1 Clicks 401 Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjAxJTI1MjBDbGlja3MlMjUyMDQwMSUyNTIwRXJyb3I

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V21Clicks401ErrorException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Required | A short identifier corresponding to the HTTP status code returned. For  example, the ID for a response returning a 404 status code would be "not_found." |
| `message` | `String` | Required | A message providing additional information about the error, including  details to help resolve it when possible. |
| `request_id` | `String` | Optional | Optionally, some endpoints may include a request ID that should be  provided when reporting bugs or opening support tickets to help  identify the issue. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
begin
  # make the API call
rescue V21Clicks401ErrorException => e
  puts "Caught V21Clicks401ErrorException: #{e.message}"
end
```



