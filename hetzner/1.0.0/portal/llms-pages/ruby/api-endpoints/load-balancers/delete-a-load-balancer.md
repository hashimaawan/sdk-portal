# Delete a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkRlbGV0ZSUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXI

Deletes a Load Balancer.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def delete_a_load_balancer(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Load Balancer |


# Response Type

**204**: Load Balancer deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
id = 112

result = load_balancers_api.delete_a_load_balancer(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



