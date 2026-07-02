# Resources 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc291cmNlczM

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Resources3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_id` | `String` | Optional | The identifier of a resource. |
| `resource_type` | [`ResourceType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/resource-type-2.md) | Optional | The type of the resource. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
resources3 = Resources3.new(
  resource_id: '3d80cb72-342b-4aaa-b92e-4e4abb24a933',
  resource_type: ResourceType2::VOLUME,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



