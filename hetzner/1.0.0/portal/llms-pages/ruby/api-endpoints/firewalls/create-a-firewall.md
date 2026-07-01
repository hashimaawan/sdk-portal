# Create a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkNyZWF0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Creates a new Firewall.

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `server_already_added`        | Server added more than one time to resource                   |
| `incompatible_network_type`   | The Network type is incompatible for the given resource       |
| `firewall_resource_not_found` | The resource the Firewall should be attached to was not found |

:information_source: **Note** This endpoint does not require authentication.

```ruby
def create_a_firewall(body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateFirewallRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/create-firewall-request.md) | Body, Optional | - |


# Response Type

**201**: The `firewall` key contains the Firewall that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`CreateFirewallResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/create-firewall-response.md).


# Example Usage

```ruby
body = CreateFirewallRequest.new(
  name: 'Corporate Intranet Protection',
  apply_to: [
    ApplyTo.new(
      type: Type7::SERVER,
      server: Server2.new(
        id: 42
      )
    )
  ],
  labels: { 'env' => 'dev' },
  rules: [
    Rule.new(
      direction: Direction::ENUM_IN,
      protocol: Protocol::TCP,
      description: 'Allow port 80',
      port: '80',
      source_ips: [
        '28.239.13.1/32',
        '28.239.14.0/24',
        'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
      ]
    )
  ]
)

result = firewalls_api.create_a_firewall(body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



