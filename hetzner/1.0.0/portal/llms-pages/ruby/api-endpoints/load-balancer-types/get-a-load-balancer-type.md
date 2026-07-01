# Get a Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyRkdldCUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXIlMjUyMFR5cGU

Gets a specific Load Balancer type object.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_a_load_balancer_type(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of Load Balancer type |


# Response Type

**200**: The `load_balancer_type` key in the reply contains a Load Balancer type object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`LoadBalancerTypesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-types-response-1.md).


# Example Usage

```ruby
id = 112

result = load_balancer_types_api.get_a_load_balancer_type(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



