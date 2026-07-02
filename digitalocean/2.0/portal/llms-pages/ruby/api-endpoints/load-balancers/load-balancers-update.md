# Load Balancers Update

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRmxvYWRCYWxhbmNlcnNfdXBkYXRl

To update a load balancer's settings, send a PUT request to
`/v2/load_balancers/$LOAD_BALANCER_ID`. The request should contain a full
representation of the load balancer including existing attributes. It may
contain _one of_ the `droplets_ids` or `tag` attributes as they are mutually
exclusive. **Note that any attribute that is not provided will be reset to its
default value.**

```ruby
def load_balancers_update(lb_id,
                          body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lb_id` | `String` | Template, Required | A unique identifier for a load balancer. |
| `body` | [Assign Droplets by ID](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/assign-droplets-by-id.md) \| [Assign Droplets by Tag](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/assign-droplets-by-tag.md) | Body, Required | This is a container for one-of cases. |


# Response Type

**200**: The response will be a JSON object with a key called `load_balancer`. The
value of this will be an object containing the standard attributes of a
load balancer.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2LoadBalancersResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-load-balancers-response-1.md).


# Example Usage

```ruby
lb_id = '4de7ac8b-495b-4884-9a69-1050c6793cd6'

body = AssignDropletsById.new(
  droplet_ids: [
    3164444,
    3164445
  ],
  region: Region2::NYC3,
  forwarding_rules: [
    ForwardingRule.new(
      entry_port: 80,
      entry_protocol: EntryProtocol::HTTP,
      target_port: 80,
      target_protocol: TargetProtocol::HTTP,
      certificate_id: '',
      tls_passthrough: false
    ),
    ForwardingRule.new(
      entry_port: 443,
      entry_protocol: EntryProtocol::HTTPS,
      target_port: 443,
      target_protocol: TargetProtocol::HTTPS,
      certificate_id: '',
      tls_passthrough: true
    )
  ],
  algorithm: Algorithm::ROUND_ROBIN,
  enable_backend_keepalive: true,
  enable_proxy_protocol: true,
  firewall: Firewall1.new(
    allow: [
      'ip:1.2.3.4',
      'cidr:2.3.4.0/24'
    ],
    deny: [
      'cidr:1.2.0.0/16',
      'ip:2.3.4.5'
    ]
  ),
  health_check: HealthCheck1.new(
    check_interval_seconds: 10,
    healthy_threshold: 5,
    path: '/',
    port: 80,
    protocol: Protocol1::HTTP,
    response_timeout_seconds: 5,
    unhealthy_threshold: 3
  ),
  http_idle_timeout_seconds: 60,
  name: 'updated-example-lb-01',
  project_id: '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
  redirect_http_to_https: false,
  sticky_sessions: StickySessions.new(
    type: Type16::NONE
  ),
  vpc_uuid: 'c33931f2-a26a-4e61-b85c-4e95a2ec431b'
)

result = load_balancers_api.load_balancers_update(
  lb_id,
  body
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
  "load_balancer": {
    "algorithm": "round_robin",
    "created_at": "2017-02-01T22:22:58Z",
    "disable_lets_encrypt_dns_records": false,
    "droplet_ids": [
      3164444,
      3164445
    ],
    "enable_backend_keepalive": true,
    "enable_proxy_protocol": true,
    "firewall": {
      "allow": [
        "ip:1.2.3.4",
        "cidr:2.3.4.0/24"
      ],
      "deny": [
        "cidr:1.2.0.0/16",
        "ip:2.3.4.5"
      ]
    },
    "forwarding_rules": [
      {
        "certificate_id": "",
        "entry_port": 80,
        "entry_protocol": "http",
        "target_port": 80,
        "target_protocol": "http",
        "tls_passthrough": false
      },
      {
        "certificate_id": "",
        "entry_port": 443,
        "entry_protocol": "https",
        "target_port": 443,
        "target_protocol": "https",
        "tls_passthrough": true
      }
    ],
    "health_check": {
      "check_interval_seconds": 10,
      "healthy_threshold": 5,
      "path": "/",
      "port": 80,
      "protocol": "http",
      "response_timeout_seconds": 5,
      "unhealthy_threshold": 3
    },
    "http_idle_timeout_seconds": 60,
    "id": "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    "ip": "104.131.186.241",
    "name": "updated-example-lb-01",
    "project_id": "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    "redirect_http_to_https": false,
    "region": {
      "available": true,
      "features": [
        "private_networking",
        "backups",
        "ipv6",
        "metadata",
        "install_agent"
      ],
      "name": "New York 3",
      "sizes": [
        "s-1vcpu-1gb",
        "s-1vcpu-2gb",
        "s-1vcpu-3gb",
        "s-2vcpu-2gb",
        "s-3vcpu-1gb",
        "s-2vcpu-4gb",
        "s-4vcpu-8gb",
        "s-6vcpu-16gb",
        "s-8vcpu-32gb",
        "s-12vcpu-48gb",
        "s-16vcpu-64gb",
        "s-20vcpu-96gb",
        "s-24vcpu-128gb",
        "s-32vcpu-192gb"
      ],
      "slug": "nyc3"
    },
    "size": "lb-small",
    "status": "new",
    "sticky_sessions": {
      "type": "none"
    },
    "tag": "",
    "vpc_uuid": "c33931f2-a26a-4e61-b85c-4e95a2ec431b"
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



