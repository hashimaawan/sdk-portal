# Get All Load Balancer Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyRkdldCUyNTIwYWxsJTI1MjBMb2FkJTI1MjBCYWxhbmNlciUyNTIwVHlwZXM

Gets all Load Balancer type objects.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_load_balancer_types(self,
                               name=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Query, Optional | Can be used to filter Load Balancer types by their name. The response will only contain the Load Balancer type matching the specified name. |


# Response Type

**200**: The `load_balancer_types` key in the reply contains an array of Load Balancer type objects with this structure

[`LoadBalancerTypesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer-types-response.md)


# Example Usage

```python
result = load_balancer_types_controller.get_all_load_balancer_types()
print(result)
```



