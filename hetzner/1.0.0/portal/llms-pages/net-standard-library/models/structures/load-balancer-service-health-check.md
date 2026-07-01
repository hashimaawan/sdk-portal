# Load Balancer Service Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIZWFsdGhDaGVjaw

Service health check


# Class Name

`LoadBalancerServiceHealthCheck`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Http` | [`Http`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/http.md) | Optional | Additional configuration for protocol http |
| `Interval` | `int` | Required | Time interval in seconds health checks are performed |
| `Port` | `int` | Required | Port the health check will be performed on |
| `Protocol` | [`Protocol6Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/protocol-6.md) | Required | Type of the health check |
| `Retries` | `int` | Required | Unsuccessful retries needed until a target is considered unhealthy; an unhealthy target needs the same number of successful retries to become healthy again |
| `Timeout` | `int` | Required | Time in seconds after an attempt is considered a timeout |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

LoadBalancerServiceHealthCheck loadBalancerServiceHealthCheck = new LoadBalancerServiceHealthCheck
{
    Interval = 15,
    Port = 4711,
    Protocol = Protocol6Enum.Http,
    Retries = 3,
    Timeout = 10,
    Http = new Http
    {
        Domain = "domain4",
        Path = "path2",
        Response = "response8",
        StatusCodes = new List<string>
        {
            "status_codes0",
            "status_codes1",
            "status_codes2",
        },
        Tls = false,
    },
};
```



