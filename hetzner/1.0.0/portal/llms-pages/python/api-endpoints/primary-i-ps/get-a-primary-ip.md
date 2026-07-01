# Get a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkdldCUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Returns a specific Primary IP object.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_a_primary_ip(self,
                    id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**200**: The `primary_ip` key contains a Primary IP object

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`PrimaryIpResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/primary-ip-response.md).


# Example Usage

```python
id = 112

result = primary_i_ps_api.get_a_primary_ip(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



