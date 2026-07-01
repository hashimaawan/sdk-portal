# Load Balancer Target Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldFNlcnZlcg

Server where the traffic should be routed through

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancerTargetServer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Required | ID of the Server |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancer_target_server = LoadBalancerTargetServer.new(
  id: 80,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



