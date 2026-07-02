# Pages 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlBhZ2VzMQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Pages1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `first` | `String` | Optional | URI of the first page of the results. |
| `prev` | `String` | Optional | URI of the previous page of the results. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
pages1 = Pages1.new(
  first: 'https://api.digitalocean.com/v2/images?page=1',
  prev: 'https://api.digitalocean.com/v2/images?page=1',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



