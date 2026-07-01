# Get a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkdldCUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXI

Gets a specific Load Balancer object.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_a_load_balancer(self,
                       id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |


# Response Type

**200**: The `load_balancer` key contains the Load Balancer

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`LoadBalancersResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancers-response-2.md).


# Example Usage

```python
id = 112

result = load_balancers_api.get_a_load_balancer(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



