# Get All Actions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkFjdGlvbnMlMkZHZXQlMjUyMGFsbCUyNTIwQWN0aW9ucw

Returns all Action objects. You can `sort` the results by using the sort URI parameter, and filter them with the `status` parameter.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_actions(self,
                   id=None,
                   sort=None,
                   status=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Query, Optional | Can be used multiple times, the response will contain only Actions with specified IDs |
| `sort` | [`ParameterSort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/parameter-sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`ParameterStatus`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/parameter-status.md) | Query, Optional | Can be used multiple times, the response will contain only Actions with specified statuses |


# Response Type

**200**: The `actions` key contains a list of Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/actions-response.md).


# Example Usage

```python
result = actions_api.get_all_actions()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



