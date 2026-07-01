# Get a Datacenter

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkRhdGFjZW50ZXJzJTJGR2V0JTI1MjBhJTI1MjBEYXRhY2VudGVy

Returns a specific Datacenter object.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_a_datacenter(self,
                    id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of Datacenter |


# Response Type

**200**: The `datacenter` key in the reply contains a Datacenter object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`DatacentersResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/datacenters-response-1.md).


# Example Usage

```python
id = 112

result = datacenters_api.get_a_datacenter(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



