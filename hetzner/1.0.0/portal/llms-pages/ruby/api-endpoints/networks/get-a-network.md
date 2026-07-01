# Get a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGR2V0JTI1MjBhJTI1MjBOZXR3b3Jr

Gets a specific network object.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_a_network(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the network |


# Response Type

**200**: The `network` key contains the network

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`NetworksResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/networks-response-1.md).


# Example Usage

```ruby
id = 112

result = networks_api.get_a_network(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



