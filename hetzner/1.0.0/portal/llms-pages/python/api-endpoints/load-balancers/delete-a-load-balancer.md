# Delete a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkRlbGV0ZSUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXI

Deletes a Load Balancer.

:information_source: **Note** This endpoint does not require authentication.

```python
def delete_a_load_balancer(self,
                          id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |


# Response Type

**204**: Load Balancer deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
id = 112

result = load_balancers_api.delete_a_load_balancer(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



