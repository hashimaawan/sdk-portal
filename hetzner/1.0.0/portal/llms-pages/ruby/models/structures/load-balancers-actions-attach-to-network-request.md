# Load Balancers Actions Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQXR0YWNoJTI1MjBUbyUyNTIwTmV0d29yayUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancersActionsAttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | `String` | Optional | IP to request to be assigned to this Load Balancer; if you do not provide this then you will be auto assigned an IP address |
| `network` | `Float` | Required | ID of an existing network to attach the Load Balancer to |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancers_actions_attach_to_network_request = LoadBalancersActionsAttachToNetworkRequest.new(
  network: 4711,
  ip: '10.0.1.1',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



