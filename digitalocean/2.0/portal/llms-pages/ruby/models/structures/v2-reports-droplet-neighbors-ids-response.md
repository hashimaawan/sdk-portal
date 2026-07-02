# V2 Reports Droplet Neighbors Ids Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBSZXBvcnRzJTI1MjBEcm9wbGV0JTI1MjBOZWlnaGJvcnMlMjUyMElkcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2ReportsDropletNeighborsIdsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `neighbor_ids` | `Array[Integer]` | Optional | An array of arrays. Each array will contain a set of Droplet IDs for Droplets that share a physical server. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_reports_droplet_neighbors_ids_response = V2ReportsDropletNeighborsIdsResponse.new(
  neighbor_ids: [
    [
      168671828,
      168663509,
      168671815
    ],
    [
      168671883,
      168671750
    ]
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



