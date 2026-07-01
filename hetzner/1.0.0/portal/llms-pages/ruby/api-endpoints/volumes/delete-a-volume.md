# Delete a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZEZWxldGUlMjUyMGElMjUyMFZvbHVtZQ

Deletes a volume. All Volume data is irreversibly destroyed. The Volume must not be attached to a Server and it must not have delete protection enabled.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def delete_a_volume(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | ID of the Volume |


# Response Type

**204**: Volume deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
id = 'id0'

result = volumes_api.delete_a_volume(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



