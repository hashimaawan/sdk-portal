# V2 Load Balancers Droplets Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMERyb3BsZXRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2LoadBalancersDropletsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet_ids` | `Array[Integer]` | Optional | An array containing the IDs of the Droplets assigned to the load balancer. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_load_balancers_droplets_request = V2LoadBalancersDropletsRequest.new(
  droplet_ids: [
    3164444,
    3164445
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



