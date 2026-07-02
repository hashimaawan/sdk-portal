# Mongodb 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRk1vbmdvZGIx

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Mongodb1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `end_of_availability` | `String` | Optional | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. |
| `end_of_life` | `String` | Optional | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. |
| `version` | `String` | Optional | The engine version. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
mongodb1 = Mongodb1.new(
  end_of_availability: '2023-05-09T00:00:00Z',
  end_of_life: '2023-11-09T00:00:00Z',
  version: '8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



