# V2 Volumes Actions Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2VolumesActionsRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/region-2.md) | Optional | The slug identifier for the region where the resource will initially be  available. |
| `type` | [`Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/type-21.md) | Required | The volume action to initiate. |
| `droplet_id` | `Integer` | Required | The unique identifier for the Droplet the volume will be attached or detached from. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_volumes_actions_request1 = V2VolumesActionsRequest1.new(
  type: Type21::ATTACH,
  droplet_id: 11612190,
  region: Region2::NYC3,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



