# V2 Vpcs Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBWcGNzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2VpcsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | A free-form text field for describing the VPC's purpose. It may be a maximum of 255 characters.<br><br>**Constraints**: *Maximum Length*: `255` |
| `name` | `String` | Required | The name of the VPC. Must be unique and may only contain alphanumeric characters, dashes, and periods.<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9\-\.]+$` |
| `ip_range` | `String` | Optional | The range of IP addresses in the VPC in CIDR notation. Network ranges cannot overlap with other networks in the same account and must be in range of private addresses as defined in RFC1918. It may not be smaller than `/28` nor larger than `/16`. If no IP range is specified, a `/20` network range is generated that won't conflict with other VPC networks in your account. |
| `region` | `String` | Required | The slug identifier for the region where the VPC will be created. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_vpcs_request = V2VpcsRequest.new(
  name: 'env.prod-vpc',
  region: 'nyc1',
  description: 'VPC for production environment',
  ip_range: '10.10.10.0/24',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



