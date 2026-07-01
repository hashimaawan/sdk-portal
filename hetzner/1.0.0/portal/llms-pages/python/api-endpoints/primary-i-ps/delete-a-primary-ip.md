# Delete a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkRlbGV0ZSUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Deletes a Primary IP.

The Primary IP may be assigned to a Server. In this case it is unassigned automatically. The Server must be powered off (status `off`) in order for this operation to succeed.

:information_source: **Note** This endpoint does not require authentication.

```python
def delete_a_primary_ip(self,
                       id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**204**: Primary IP deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
id = 112

result = primary_i_ps_api.delete_a_primary_ip(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



