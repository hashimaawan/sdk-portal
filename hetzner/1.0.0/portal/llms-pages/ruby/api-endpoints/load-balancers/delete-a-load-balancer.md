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

`void`


# Example Usage

```ruby
id = 112

load_balancers_controller.delete_a_load_balancer(id)
```



