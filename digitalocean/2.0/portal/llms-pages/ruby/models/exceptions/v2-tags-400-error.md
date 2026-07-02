# V2 Tags 400 Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjA0MDAlMjUyMEVycm9y

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2Tags400ErrorException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | `String` | Required | A message providing information about the error. |
| `messages` | `Array[String]` | Optional | A list of error messages. |
| `root_causes` | `Array[String]` | Required | A list of underlying causes for the error, including details to help  resolve it when possible. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
begin
  # make the API call
rescue V2Tags400ErrorException => e
  puts "Caught V2Tags400ErrorException: #{e.message}"
end
```



