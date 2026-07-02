# Firewalls Update

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRmZpcmV3YWxsc191cGRhdGU

To update the configuration of an existing firewall, send a PUT request to
`/v2/firewalls/$FIREWALL_ID`. The request should contain a full representation
of the firewall including existing attributes. **Note that any attributes that
are not provided will be reset to their default values.**

```ruby
def firewalls_update(firewall_id,
                     body: nil)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewall_id` | `UUID \| String` | Template, Required | A unique ID that can be used to identify and reference a firewall. |
| `body` | [`V2FirewallsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-firewalls-request.md) | Body, Optional | - |


# Response Type

**200**: The response will be a JSON object with a `firewall` key. This will be set to an object containing the standard firewall attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2FirewallsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-firewalls-response-1.md).


# Example Usage

```ruby
firewall_id = 'bb4b2611-3d72-467b-8602-280330ecd65c'

body = V2FirewallsRequest.new(
  name: 'frontend-firewall',
  inbound_rules: [
    InboundRule.new(
      ports: '8080',
      protocol: Protocol::TCP,
      sources: Sources.new(
        load_balancer_uids: [
          '4de7ac8b-495b-4884-9a69-1050c6793cd6'
        ]
      )
    ),
    InboundRule.new(
      ports: '22',
      protocol: Protocol::TCP,
      sources: Sources.new(
        addresses: [
          '18.0.0.0/8'
        ],
        tags: [
          'gateway'
        ]
      )
    )
  ],
  outbound_rules: [
    OutboundRule.new(
      ports: '8080',
      protocol: Protocol::TCP,
      destinations: Destinations.new(
        addresses: [
          '0.0.0.0/0',
          '::/0'
        ]
      )
    )
  ],
  droplet_ids: [
    8043964
  ],
  tags: [
    'frontend'
  ]
)

result = firewalls_api.firewalls_update(
  firewall_id,
  body: body
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Example Response *(as JSON)*

```json
{
  "firewall": {
    "created_at": "2020-05-23T21:24:00Z",
    "droplet_ids": [
      8043964
    ],
    "id": "bb4b2611-3d72-467b-8602-280330ecd65c",
    "inbound_rules": [
      {
        "ports": "80",
        "protocol": "tcp",
        "sources": {
          "load_balancer_uids": [
            "4de7ac8b-495b-4884-9a69-1050c6793cd6"
          ]
        }
      },
      {
        "ports": "22",
        "protocol": "tcp",
        "sources": {
          "addresses": [
            "18.0.0.0/8"
          ],
          "tags": [
            "gateway"
          ]
        }
      }
    ],
    "name": "frontend-firewall",
    "outbound_rules": [
      {
        "destinations": {
          "addresses": [
            "0.0.0.0/0",
            "::/0"
          ]
        },
        "ports": "80",
        "protocol": "tcp"
      }
    ],
    "pending_changes": [
      {
        "droplet_id": 8043964,
        "removing": false,
        "status": "waiting"
      }
    ],
    "status": "waiting",
    "tags": [
      "frontend"
    ]
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



