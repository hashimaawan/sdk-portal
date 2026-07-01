# Get a Location

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkxvY2F0aW9ucyUyRkdldCUyNTIwYSUyNTIwTG9jYXRpb24

Returns a specific Location object.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_a_location(self,
                  id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of Location |


# Response Type

**200**: The `location` key in the reply contains a Location object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`LocationsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/locations-response-1.md).


# Example Usage

```python
id = 112

result = locations_api.get_a_location(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



