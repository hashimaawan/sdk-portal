# Get All Locations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkxvY2F0aW9ucyUyRkdldCUyNTIwYWxsJTI1MjBMb2NhdGlvbnM

Returns all Location objects.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_locations(self,
                     name=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Query, Optional | Can be used to filter Locations by their name. The response will only contain the Location matching the specified name. |


# Response Type

**200**: The `locations` key in the reply contains an array of Location objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`LocationsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/locations-response.md).


# Example Usage

```python
result = locations_api.get_all_locations()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



