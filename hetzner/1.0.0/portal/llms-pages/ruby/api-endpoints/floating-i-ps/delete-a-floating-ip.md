# Delete a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZEZWxldGUlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Deletes a Floating IP. If it is currently assigned to a Server it will automatically get unassigned.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def delete_a_floating_ip(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Floating IP |


# Response Type

**204**: Floating IP deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
id = 112

result = floating_i_ps_api.delete_a_floating_ip(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



