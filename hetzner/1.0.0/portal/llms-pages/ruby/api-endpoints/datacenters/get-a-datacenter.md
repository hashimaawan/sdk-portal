# Get a Datacenter

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkRhdGFjZW50ZXJzJTJGR2V0JTI1MjBhJTI1MjBEYXRhY2VudGVy

Returns a specific Datacenter object.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_a_datacenter(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of Datacenter |


# Response Type

**200**: The `datacenter` key in the reply contains a Datacenter object with this structure

[`DatacentersResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/datacenters-response-1.md)


# Example Usage

```ruby
id = 112

result = datacenters_controller.get_a_datacenter(id)
puts result
```



