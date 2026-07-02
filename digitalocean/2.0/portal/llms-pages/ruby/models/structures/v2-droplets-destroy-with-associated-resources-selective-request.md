# V2 Droplets Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing information about a resource to be scheduled for deletion.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floating_ips` | `Array[String]` | Optional | An array of unique identifiers for the floating IPs to be scheduled for deletion. |
| `reserved_ips` | `Array[String]` | Optional | An array of unique identifiers for the reserved IPs to be scheduled for deletion. |
| `snapshots` | `Array[String]` | Optional | An array of unique identifiers for the snapshots to be scheduled for deletion. |
| `volume_snapshots` | `Array[String]` | Optional | An array of unique identifiers for the volume snapshots to be scheduled for deletion. |
| `volumes` | `Array[String]` | Optional | An array of unique identifiers for the volumes to be scheduled for deletion. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_droplets_destroy_with_associated_resources_selective_request = V2DropletsDestroyWithAssociatedResourcesSelectiveRequest.new(
  floating_ips: [
    '6186916'
  ],
  reserved_ips: [
    '6186916'
  ],
  snapshots: [
    '61486916'
  ],
  volume_snapshots: [
    'edb0478d-7436-11ea-86e6-0a58ac144b91'
  ],
  volumes: [
    'ba49449a-7435-11ea-b89e-0a58ac14480f'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



