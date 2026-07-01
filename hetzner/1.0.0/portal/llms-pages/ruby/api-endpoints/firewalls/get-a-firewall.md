# Get a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkdldCUyNTIwYSUyNTIwRmlyZXdhbGw

Gets a specific Firewall object.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_a_firewall(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the resource |


# Response Type

**200**: The `firewall` key contains a Firewall object

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`FirewallResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/firewall-response.md).


# Example Usage

```ruby
id = 112

result = firewalls_api.get_a_firewall(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



