# Reserve to Region 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc2VydmUlMjUyMHRvJTI1MjBSZWdpb24x

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`ReserveToRegion1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `project_id` | `UUID \| String` | Optional | The UUID of the project to which the reserved IP will be assigned. |
| `region` | `String` | Required | The slug identifier for the region the reserved IP will be reserved to. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
reserve_to_region1 = ReserveToRegion1.new(
  region: 'nyc3',
  project_id: '746c6152-2fa2-11ed-92d3-27aaa54e4988',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



