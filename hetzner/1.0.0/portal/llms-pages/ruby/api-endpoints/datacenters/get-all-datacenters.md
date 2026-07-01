# Get All Datacenters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkRhdGFjZW50ZXJzJTJGR2V0JTI1MjBhbGwlMjUyMERhdGFjZW50ZXJz

Returns all Datacenter objects.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_all_datacenters(name: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Query, Optional | Can be used to filter Datacenters by their name. The response will only contain the Datacenter matching the specified name. When the name does not match the Datacenter name format, an `invalid_input` error is returned. |


# Response Type

**200**: The reply contains the `datacenters` and `recommendation` keys

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`DatacentersResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/datacenters-response.md).


# Example Usage

```ruby
result = datacenters_api.get_all_datacenters

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



