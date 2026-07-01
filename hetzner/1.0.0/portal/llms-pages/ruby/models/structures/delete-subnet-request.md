# Delete Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkRlbGV0ZVN1Ym5ldFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`DeleteSubnetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip_range` | `String` | Required | IP range of subnet to delete |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
delete_subnet_request = DeleteSubnetRequest.new(
  ip_range: '10.0.1.0/24',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



