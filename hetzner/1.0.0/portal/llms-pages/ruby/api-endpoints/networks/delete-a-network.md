# Delete a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGRGVsZXRlJTI1MjBhJTI1MjBOZXR3b3Jr

Deletes a network. If there are Servers attached they will be detached in the background.

Note: if the network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def delete_a_network(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the network |


# Response Type

**204**: Network deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
id = 112

result = networks_api.delete_a_network(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



