# Load Balancers Get

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRmxvYWRCYWxhbmNlcnNfZ2V0

To show information about a load balancer instance, send a GET request to
`/v2/load_balancers/$LOAD_BALANCER_ID`.

```python
def load_balancers_get(self,
                      lb_id)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lb_id` | `str` | Template, Required | A unique identifier for a load balancer. |


# Response Type

**200**: The response will be a JSON object with a key called `load_balancer`. The
value of this will be an object that contains the standard attributes
associated with a load balancer

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2LoadBalancersResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-load-balancers-response-1.md).


# Example Usage

```python
lb_id = '4de7ac8b-495b-4884-9a69-1050c6793cd6'

result = load_balancers_api.load_balancers_get(lb_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
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
    "enable_backend_keepalive": false,
    "enable_proxy_protocol": false,
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
    "name": "example-lb-01",
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



