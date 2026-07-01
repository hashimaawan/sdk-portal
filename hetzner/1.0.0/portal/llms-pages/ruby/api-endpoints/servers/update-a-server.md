# Update a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZVcGRhdGUlMjUyMGElMjUyMFNlcnZlcg

Updates a Server. You can update a Server’s name and a Server’s labels.
Please note that Server names must be unique per Project and valid hostnames as per RFC 1123 (i.e. may only contain letters, digits, periods, and dashes).
Also note that when updating labels, the Server’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def update_a_server(id,
                    body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Server |
| `body` | [`UpdateServerRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/update-server-request.md) | Body, Optional | - |


# Response Type

**200**: The `server` key in the reply contains the updated Server

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ServersResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/servers-response-2.md).


# Example Usage

```ruby
id = 112

body = UpdateServerRequest.new(
  labels: { 'labelkey' => 'value' },
  name: 'my-server'
)

result = servers_api.update_a_server(
  id,
  body: body
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



