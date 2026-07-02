# V2 Firewalls Tags Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFRhZ3MlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2FirewallsTagsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tags` | `Array[String]` | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_firewalls_tags_request = V2FirewallsTagsRequest.new(
  tags: [
    'tags5',
    'tags6',
    'tags7'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



