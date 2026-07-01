# Delete a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZEZWxldGUlMjUyMGElMjUyMFNlcnZlcg

Deletes a Server. This immediately removes the Server from your account, and it is no longer accessible.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def delete_a_server(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Server |


# Response Type

**200**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ServersResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/servers-response-1.md).


# Example Usage

```ruby
id = 112

result = servers_api.delete_a_server(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



