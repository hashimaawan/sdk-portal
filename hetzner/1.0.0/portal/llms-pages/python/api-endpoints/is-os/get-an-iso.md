# Get an ISO

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRklTT3MlMkZHZXQlMjUyMGFuJTI1MjBJU08

Returns a specific ISO object.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_an_iso(self,
              id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the ISO |


# Response Type

**200**: The `iso` key in the reply contains an array of ISO objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`IsosResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/isos-response-1.md).


# Example Usage

```python
id = 112

result = is_os_api.get_an_iso(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



