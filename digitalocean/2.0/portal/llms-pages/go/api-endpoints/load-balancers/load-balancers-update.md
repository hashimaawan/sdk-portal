# Load Balancers Update

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRmxvYWRCYWxhbmNlcnNfdXBkYXRl

To update a load balancer's settings, send a PUT request to
`/v2/load_balancers/$LOAD_BALANCER_ID`. The request should contain a full
representation of the load balancer including existing attributes. It may
contain _one of_ the `droplets_ids` or `tag` attributes as they are mutually
exclusive. **Note that any attribute that is not provided will be reset to its
default value.**

```go
LoadBalancersUpdate(
    ctx context.Context,
    lbId string,
    body models.LoadBalancersUpdateBody) (
    models.ApiResponse[models.V2LoadBalancersResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lbId` | `string` | Template, Required | A unique identifier for a load balancer. |
| `body` | [`models.LoadBalancersUpdateBody`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/load-balancers-update-body.md) | Body, Required | This is a container for one-of cases. |


# Response Type

**200**: The response will be a JSON object with a key called `load_balancer`. The
value of this will be an object containing the standard attributes of a
load balancer.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2LoadBalancersResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-load-balancers-response-1.md).


# Example Usage

```go
ctx := context.Background()

lbId := "4de7ac8b-495b-4884-9a69-1050c6793cd6"

body := models.LoadBalancersUpdateBodyContainer.FromAssignDropletsById(models.AssignDropletsById{
    DropletIds:                   []int{
        3164444,
        3164445,
    },
    Region:                       models.Region2_Nyc3,
    Algorithm:                    models.ToPointer(models.Algorithm_RoundRobin),
    EnableBackendKeepalive:       models.ToPointer(true),
    EnableProxyProtocol:          models.ToPointer(true),
    Firewall:                     models.ToPointer(models.Firewall1{
        Allow:                 []string{
            "ip:1.2.3.4",
            "cidr:2.3.4.0/24",
        },
        Deny:                  []string{
            "cidr:1.2.0.0/16",
            "ip:2.3.4.5",
        },
    }),
    ForwardingRules:              []models.ForwardingRule{
        models.ForwardingRule{
            CertificateId:         models.ToPointer(""),
            EntryPort:             80,
            EntryProtocol:         models.EntryProtocol_Http,
            TargetPort:            80,
            TargetProtocol:        models.TargetProtocol_Http,
            TlsPassthrough:        models.ToPointer(false),
        },
        models.ForwardingRule{
            CertificateId:         models.ToPointer(""),
            EntryPort:             443,
            EntryProtocol:         models.EntryProtocol_Https,
            TargetPort:            443,
            TargetProtocol:        models.TargetProtocol_Https,
            TlsPassthrough:        models.ToPointer(true),
        },
    },
    HealthCheck:                  models.ToPointer(models.HealthCheck1{
        CheckIntervalSeconds:   models.ToPointer(10),
        HealthyThreshold:       models.ToPointer(5),
        Path:                   models.ToPointer("/"),
        Port:                   models.ToPointer(80),
        Protocol:               models.ToPointer(models.Protocol1_Http),
        ResponseTimeoutSeconds: models.ToPointer(5),
        UnhealthyThreshold:     models.ToPointer(3),
    }),
    HttpIdleTimeoutSeconds:       models.ToPointer(60),
    Name:                         models.ToPointer("updated-example-lb-01"),
    ProjectId:                    models.ToPointer("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30"),
    RedirectHttpToHttps:          models.ToPointer(false),
    StickySessions:               models.ToPointer(models.StickySessions{
        Type:                  models.ToPointer(models.Type16_None),
    }),
    VpcUuid:                      models.ToPointer(uuid.MustParse("c33931f2-a26a-4e61-b85c-4e95a2ec431b")),
})

apiResponse, err := loadBalancersApi.LoadBalancersUpdate(ctx, lbId, body)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.V21Clicks401Error:
            log.Fatalln("V21Clicks401ErrorException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



