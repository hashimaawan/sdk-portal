# Update a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRlVwZGF0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Updates the Firewall.

Note that when updating labels, the Firewall's current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

Note: if the Firewall object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def update_a_firewall(id,
                      body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the resource |
| `body` | [`UpdateFirewallRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/update-firewall-request.md) | Body, Optional | - |


# Response Type

**200**: The `firewall` key contains the Firewall that was just updated

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`FirewallResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/firewall-response.md).


# Example Usage

```ruby
id = 112

body = UpdateFirewallRequest.new(
  labels: { 'labelkey' => 'value' },
  name: 'new-name'
)

result = firewalls_api.update_a_firewall(
  id,
  body: body
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



