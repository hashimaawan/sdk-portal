# Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlBhZ2Vz

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Pages`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `last` | `String` | Optional | URI of the last page of the results. |
| `mnext` | `String` | Optional | URI of the next page of the results. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
pages = Pages.new(
  last: 'https://api.digitalocean.com/v2/images?page=2',
  mnext: 'https://api.digitalocean.com/v2/images?page=2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



