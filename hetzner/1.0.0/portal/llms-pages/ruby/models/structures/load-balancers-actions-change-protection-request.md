# Load Balancers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `TrueClass \| FalseClass` | Optional | If true, prevents the Load Balancer from being deleted |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancers_actions_change_protection_request = LoadBalancersActionsChangeProtectionRequest.new(
  delete: true,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



