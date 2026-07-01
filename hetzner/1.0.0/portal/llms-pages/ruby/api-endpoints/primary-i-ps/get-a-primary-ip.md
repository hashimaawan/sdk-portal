# Get a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkdldCUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Returns a specific Primary IP object.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_a_primary_ip(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the resource |


# Response Type

**200**: The `primary_ip` key contains a Primary IP object

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`PrimaryIpResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/primary-ip-response.md).


# Example Usage

```ruby
id = 112

result = primary_i_ps_api.get_a_primary_ip(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



