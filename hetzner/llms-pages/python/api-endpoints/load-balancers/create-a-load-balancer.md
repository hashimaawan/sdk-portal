# Create a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkNyZWF0ZSUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXI

Creates a Load Balancer.

#### Call specific error codes

| Code                                    | Description                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------|
| `cloud_resource_ip_not_allowed`         | The IP you are trying to add as a target belongs to a Hetzner Cloud resource                          |
| `ip_not_owned`                          | The IP is not owned by the owner of the project of the Load Balancer                                  |
| `load_balancer_not_attached_to_network` | The Load Balancer is not attached to a network                                                        |
| `robot_unavailable`                     | Robot was not available. The caller may retry the operation after a short delay.                      |
| `server_not_attached_to_network`        | The server you are trying to add as a target is not attached to the same network as the Load Balancer |
| `source_port_already_used`              | The source port you are trying to add is already in use                                               |
| `target_already_defined`                | The Load Balancer target you are trying to define is already defined                                  |

:information_source: **Note** This endpoint does not require authentication.

```python
def create_a_load_balancer(self,
                          body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateLoadBalancerRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/create-load-balancer-request.md) | Body, Optional | - |


# Response Type

**201**: The `load_balancer` key contains the Load Balancer that was just created

[`LoadBalancersResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/load-balancers-response-1.md)


# Example Usage

```python
body = CreateLoadBalancerRequest(
    algorithm=LoadBalancerAlgorithm(
        mtype=Type28Enum.ROUND_ROBIN
    ),
    load_balancer_type='lb11',
    name='Web Frontend',
    network=123,
    network_zone='eu-central',
    public_interface=True
)

result = load_balancers_controller.create_a_load_balancer(
    body=body
)
print(result)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "create_load_balancer",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": "2016-01-30T23:56:00+00:00",
    "id": 13,
    "progress": 100,
    "resources": [
      {
        "id": 4711,
        "type": "load_balancer"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  },
  "load_balancer": {
    "algorithm": {
      "type": "round_robin"
    },
    "created": "2016-01-30T23:50:00+00:00",
    "id": 4711,
    "included_traffic": 654321,
    "ingoing_traffic": 123456,
    "labels": {
      "env": "dev"
    },
    "load_balancer_type": {
      "deprecated": "2016-01-30T23:50:00+00:00",
      "description": "LB11",
      "id": 1,
      "max_assigned_certificates": 10,
      "max_connections": 20000,
      "max_services": 5,
      "max_targets": 25,
      "name": "lb11",
      "prices": [
        {
          "location": "fsn1",
          "price_hourly": {
            "gross": "1.1900000000000000",
            "net": "1.0000000000"
          },
          "price_monthly": {
            "gross": "1.1900000000000000",
            "net": "1.0000000000"
          }
        }
      ]
    },
    "location": {
      "city": "Falkenstein",
      "country": "DE",
      "description": "Falkenstein DC Park 1",
      "id": 1,
      "latitude": 50.47612,
      "longitude": 12.370071,
      "name": "fsn1",
      "network_zone": "eu-central"
    },
    "name": "Web Frontend",
    "outgoing_traffic": 123456,
    "private_net": [
      {
        "ip": "10.0.0.2",
        "network": 4711
      }
    ],
    "protection": {
      "delete": false
    },
    "public_net": {
      "enabled": false,
      "ipv4": {
        "ip": "1.2.3.4"
      },
      "ipv6": {
        "ip": "2001:db8::1"
      }
    },
    "services": [
      {
        "destination_port": 80,
        "health_check": {
          "http": {
            "domain": "example.com",
            "path": "/",
            "response": "{\"status\": \"ok\"}",
            "status_codes": [
              "2??,3??"
            ],
            "tls": false
          },
          "interval": 15,
          "port": 4711,
          "protocol": "http",
          "retries": 3,
          "timeout": 10
        },
        "http": {
          "certificates": [
            897
          ],
          "cookie_lifetime": 300,
          "cookie_name": "HCLBSTICKY",
          "redirect_http": true,
          "sticky_sessions": true
        },
        "listen_port": 443,
        "protocol": "http",
        "proxyprotocol": false
      }
    ],
    "targets": [
      {
        "health_status": [
          {
            "listen_port": 443,
            "status": "healthy"
          }
        ],
        "server": {
          "id": 80
        },
        "targets": [
          {
            "health_status": [
              {
                "listen_port": 443,
                "status": "healthy"
              }
            ],
            "label_selector": null,
            "server": {
              "id": 80
            },
            "type": "server",
            "use_private_ip": true
          }
        ],
        "type": "server",
        "use_private_ip": true
      }
    ]
  }
}
```



