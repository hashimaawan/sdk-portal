# Change Loadbalancer Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNoYW5nZUxvYWRiYWxhbmNlckRuc1B0clJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`ChangeLoadbalancerDnsPtrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Required | Hostname to set as a reverse DNS PTR entry |
| `ip` | `String` | Required | Public IP address for which the reverse DNS entry should be set |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
change_loadbalancer_dns_ptr_request = ChangeLoadbalancerDnsPtrRequest.new(
  dns_ptr: 'lb1.example.com',
  ip: '1.2.3.4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



