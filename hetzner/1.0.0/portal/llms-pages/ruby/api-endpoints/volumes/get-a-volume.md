# Get a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZHZXQlMjUyMGElMjUyMFZvbHVtZQ

Gets a specific Volume object.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_a_volume(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Volume |


# Response Type

**200**: The `volume` key contains the volume

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`VolumesResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/volumes-response-2.md).


# Example Usage

```ruby
id = 112

result = volumes_api.get_a_volume(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



