# Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkF0dGFjaFRvTmV0d29ya1JlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`AttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alias_ips` | `Array[String]` | Optional | Additional IPs to be assigned to this Server |
| `ip` | `String` | Optional | IP to request to be assigned to this Server; if you do not provide this then you will be auto assigned an IP address |
| `network` | `Integer` | Required | ID of an existing network to attach the Server to |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
attach_to_network_request = AttachToNetworkRequest.new(
  network: 4711,
  alias_ips: [
    '10.0.1.2'
  ],
  ip: '10.0.1.1',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



