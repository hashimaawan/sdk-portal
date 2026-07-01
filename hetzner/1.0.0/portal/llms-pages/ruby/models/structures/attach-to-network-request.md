# Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkF0dGFjaFRvTmV0d29ya1JlcXVlc3Q


# Class Name

`AttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alias_ips` | `Array[String]` | Optional | Additional IPs to be assigned to this Server |
| `ip` | `String` | Optional | IP to request to be assigned to this Server; if you do not provide this then you will be auto assigned an IP address |
| `network` | `Integer` | Required | ID of an existing network to attach the Server to |


# Example

```ruby
attach_to_network_request = AttachToNetworkRequest.new(
  4711,
  [
    '10.0.1.2'
  ],
  '10.0.1.1'
)
```



