# Load Balancers Actions Delete Service Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGVsZXRlJTI1MjBTZXJ2aWNlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancersActionsDeleteServiceRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `listen_port` | `Float` | Required | The listen port of the service you want to delete |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancers_actions_delete_service_request = LoadBalancersActionsDeleteServiceRequest.new(
  listen_port: 4711,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



