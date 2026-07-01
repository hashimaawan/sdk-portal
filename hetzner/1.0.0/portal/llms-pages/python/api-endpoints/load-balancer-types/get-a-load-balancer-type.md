# Get a Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyRkdldCUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXIlMjUyMFR5cGU

Gets a specific Load Balancer type object.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_a_load_balancer_type(self,
                            id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of Load Balancer type |


# Response Type

**200**: The `load_balancer_type` key in the reply contains a Load Balancer type object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`LoadBalancerTypesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer-types-response-1.md).


# Example Usage

```python
id = 112

result = load_balancer_types_api.get_a_load_balancer_type(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



