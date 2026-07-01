# Get an Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkltYWdlcyUyRkdldCUyNTIwYW4lMjUyMEltYWdl

Returns a specific Image object.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_an_image(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Image |


# Response Type

**200**: The `image` key in the reply contains an Image object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ImagesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/images-response-1.md).


# Example Usage

```ruby
id = 112

result = images_api.get_an_image(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



