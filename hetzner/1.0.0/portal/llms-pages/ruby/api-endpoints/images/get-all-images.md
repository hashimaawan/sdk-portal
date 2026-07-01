# Get All Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkltYWdlcyUyRkdldCUyNTIwYWxsJTI1MjBJbWFnZXM

Returns all Image objects. You can select specific Image types only and sort the results by using URI parameters.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_all_images(sort: nil,
                   type: nil,
                   status: nil,
                   bound_to: nil,
                   include_deprecated: nil,
                   name: nil,
                   label_selector: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `type` | [`Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-21.md) | Query, Optional | Can be used multiple times. |
| `status` | [`Status23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/status-23.md) | Query, Optional | Can be used multiple times. The response will only contain Images matching the status. |
| `bound_to` | `String` | Query, Optional | Can be used multiple times. Server ID linked to the Image. Only available for Images of type `backup` |
| `include_deprecated` | `TrueClass \| FalseClass` | Query, Optional | Can be used multiple times. |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `label_selector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `images` key in the reply contains an array of Image objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ImagesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/images-response.md).


# Example Usage

```ruby
result = images_api.get_all_images

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



