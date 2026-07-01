# Get All IS Os

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRklTT3MlMkZHZXQlMjUyMGFsbCUyNTIwSVNPcw

Returns all available ISO objects.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_all_is_os(name: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Query, Optional | Can be used to filter ISOs by their name. The response will only contain the ISO matching the specified name. |


# Response Type

**200**: The `isos` key in the reply contains an array of iso objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`IsosResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/isos-response.md).


# Example Usage

```ruby
result = is_os_api.get_all_is_os

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



