# Change Loadbalancer Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNoYW5nZUxvYWRiYWxhbmNlckRuc1B0clJlcXVlc3Q


# Class Name

`ChangeLoadbalancerDnsPtrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Required | Hostname to set as a reverse DNS PTR entry |
| `ip` | `String` | Required | Public IP address for which the reverse DNS entry should be set |


# Example

```ruby
change_loadbalancer_dns_ptr_request = ChangeLoadbalancerDnsPtrRequest.new(
  'lb1.example.com',
  '1.2.3.4'
)
```



