# Get All Load Balancer Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyRkdldCUyNTIwYWxsJTI1MjBMb2FkJTI1MjBCYWxhbmNlciUyNTIwVHlwZXM

Gets all Load Balancer type objects.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_all_load_balancer_types(name: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Query, Optional | Can be used to filter Load Balancer types by their name. The response will only contain the Load Balancer type matching the specified name. |


# Response Type

**200**: The `load_balancer_types` key in the reply contains an array of Load Balancer type objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`LoadBalancerTypesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-types-response.md).


# Example Usage

```ruby
result = load_balancer_types_api.get_all_load_balancer_types

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



