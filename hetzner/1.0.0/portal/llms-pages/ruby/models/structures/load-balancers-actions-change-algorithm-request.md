# Load Balancers Actions Change Algorithm Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBBbGdvcml0aG0lMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancersActionsChangeAlgorithmRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type39`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-39.md) | Required | Algorithm of the Load Balancer |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancers_actions_change_algorithm_request = LoadBalancersActionsChangeAlgorithmRequest.new(
  type: Type39::ROUND_ROBIN,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



