# Links

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpbmtz

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Links`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pages` | [Pages](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/pages.md) \| [Pages1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/pages-1.md) \| Object \| nil | Optional | This is a container for any-of cases. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
links = Links.new(
  pages: Pages.new(
    last: 'last6',
    mnext: 'next2',
    additional_properties: {
      'pages' => JSON.parse('{"first":"https://api.digitalocean.com/v2/account/keys?page=1","prev":"https://api.digitalocean.com/v2/account/keys?page=2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



