# 1 Click

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRjFDbGljaw

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`M1Click`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `slug` | `String` | Required | The slug identifier for the 1-Click application. |
| `type` | `String` | Required | The type of the 1-Click application. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
m1_click = M1Click.new(
  slug: 'monitoring',
  type: 'kubernetes',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



