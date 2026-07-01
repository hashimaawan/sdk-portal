# Get All Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkltYWdlcyUyRkdldCUyNTIwYWxsJTI1MjBJbWFnZXM

Returns all Image objects. You can select specific Image types only and sort the results by using URI parameters.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_images(self,
                  sort=None,
                  mtype=None,
                  status=None,
                  bound_to=None,
                  include_deprecated=None,
                  name=None,
                  label_selector=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `mtype` | [`Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-21.md) | Query, Optional | Can be used multiple times. |
| `status` | [`Status23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/status-23.md) | Query, Optional | Can be used multiple times. The response will only contain Images matching the status. |
| `bound_to` | `str` | Query, Optional | Can be used multiple times. Server ID linked to the Image. Only available for Images of type `backup` |
| `include_deprecated` | `bool` | Query, Optional | Can be used multiple times. |
| `name` | `str` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `label_selector` | `str` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `images` key in the reply contains an array of Image objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ImagesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/images-response.md).


# Example Usage

```python
result = images_api.get_all_images()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



