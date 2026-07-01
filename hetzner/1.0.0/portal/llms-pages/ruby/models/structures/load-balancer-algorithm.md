# Load Balancer Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlckFsZ29yaXRobQ

Algorithm of the Load Balancer

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancerAlgorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type28`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-28.md) | Required | Type of the algorithm |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancer_algorithm = LoadBalancerAlgorithm.new(
  type: Type28::ROUND_ROBIN,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



