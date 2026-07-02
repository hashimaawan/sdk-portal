# Allow Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkFsbG93T3JpZ2lu

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`AllowOrigin`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `exact` | `String` | Optional | Exact string match. Only 1 of `exact`, `prefix`, or `regex` must be set.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `prefix` | `String` | Optional | Prefix-based match. Only 1 of `exact`, `prefix`, or `regex` must be set.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `regex` | `String` | Optional | RE2 style regex-based match. Only 1 of `exact`, `prefix`, or `regex` must be set. For more information about RE2 syntax, see: https://github.com/google/re2/wiki/Syntax<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
allow_origin = AllowOrigin.new(
  exact: 'https://www.example.com',
  prefix: 'https://www.example.com',
  regex: '^.*example.com',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



