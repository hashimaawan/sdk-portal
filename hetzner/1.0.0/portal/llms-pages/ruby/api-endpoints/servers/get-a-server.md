# Get a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZHZXQlMjUyMGElMjUyMFNlcnZlcg

Returns a specific Server object. The Server must exist inside the Project

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_a_server(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Server |


# Response Type

**200**: The `server` key in the reply contains a Server object with this structure

[`ServersResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/servers-response-2.md)


# Example Usage

```ruby
id = 112

result = servers_controller.get_a_server(id)
puts result
```



