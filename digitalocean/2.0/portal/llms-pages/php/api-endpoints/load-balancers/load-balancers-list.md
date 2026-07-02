# Load Balancers List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRmxvYWRCYWxhbmNlcnNfbGlzdA

To list all of the load balancer instances on your account, send a GET request
to `/v2/load_balancers`.

```php
function loadBalancersList(?int $perPage = 20, ?int $page = 1): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `perPage` | `?int` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `?int` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: A JSON object with a key of `load_balancers`. This will be set to an array of objects, each of which will contain the standard load balancer attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2LoadBalancersResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-load-balancers-response.md).


# Example Usage

```php
$perPage = 2;

$page = 1;

$loadBalancersApi = $client->getLoadBalancersApi();
$apiResponse = $loadBalancersApi->loadBalancersList(
    $perPage,
    $page
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2LoadBalancersResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "links": {},
  "load_balancers": [
    {
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
      "id": "4de7ac8b-495b-4884-9a69-1050c6793cd6",
      "ip": "104.131.186.241",
      "name": "example-lb-01",
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
    },
    {
      "algorithm": "round_robin",
      "created_at": "2020-09-08T18:58:04Z",
      "disable_lets_encrypt_dns_records": false,
      "droplet_ids": [
        55806512,
        55806515,
        55806524
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
          "certificate_id": "892071a0-bb95-49bc-8021-3afd67a210bf",
          "entry_port": 443,
          "entry_protocol": "https",
          "target_port": 8080,
          "target_protocol": "http",
          "tls_passthrough": false
        }
      ],
      "health_check": {
        "check_interval_seconds": 10,
        "healthy_threshold": 5,
        "path": "/",
        "port": 443,
        "protocol": "https",
        "response_timeout_seconds": 5,
        "unhealthy_threshold": 3
      },
      "http_idle_timeout_seconds": 60,
      "id": "56775c3f-04ab-4fb3-a7ed-40ef9bc8eece",
      "ip": "45.55.125.24",
      "name": "prod-web-lb-01",
      "project_id": "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
      "redirect_http_to_https": true,
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
      "status": "active",
      "sticky_sessions": {
        "cookie_name": "DO-LB",
        "cookie_ttl_seconds": 300,
        "type": "cookies"
      },
      "tag": "prod:web",
      "vpc_uuid": "587d698c-de84-11e8-80bc-3cfdfea9fcd1"
    }
  ],
  "meta": {
    "total": 2
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



