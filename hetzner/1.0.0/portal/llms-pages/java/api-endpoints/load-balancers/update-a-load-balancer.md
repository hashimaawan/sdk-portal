# Update a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRlVwZGF0ZSUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXI

Updates a Load Balancer. You can update a Load Balancer’s name and a Load Balancer’s labels.

Note that when updating labels, the Load Balancer’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

Note: if the Load Balancer object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<LoadBalancersResponse2> updateALoadBalancerAsync(
    final int id,
    final LoadBalancersRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`LoadBalancersRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancers-request.md) | Body, Optional | - |


# Response Type

**200**: The `load_balancer` key contains the updated Load Balancer

[`LoadBalancersResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancers-response-2.md)


# Example Usage

```java
int id = 112;
LoadBalancersRequest body = new LoadBalancersRequest.Builder()
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .name("new-name")
    .build();

loadBalancersController.updateALoadBalancerAsync(id, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Example Response *(as JSON)*

```json
{
  "load_balancer": {
    "algorithm": {
      "type": "round_robin"
    },
    "created": "2016-01-30T23:50:00+00:00",
    "id": 4711,
    "included_traffic": 654321,
    "ingoing_traffic": 123456,
    "labels": {
      "labelkey": "value"
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
    "name": "new-name",
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
        "ip": {
          "ip": "203.0.113.1"
        },
        "label_selector": {
          "selector": "env=prod"
        },
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



