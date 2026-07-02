# Databases

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkRhdGFiYXNlcw

Tagged Resource Statistics include metadata regarding the resource type that has been tagged.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Databases`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `count` | `Integer` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` |
| `last_tagged_uri` | `String` | Optional | The URI for the last tagged object for this type of resource. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
databases = Databases.new(
  count: 5,
  last_tagged_uri: 'https://api.digitalocean.com/v2/images/7555620',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



