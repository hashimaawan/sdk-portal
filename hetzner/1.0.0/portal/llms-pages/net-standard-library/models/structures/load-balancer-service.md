# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U

*This model accepts additional fields of type object.*


# Class Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DestinationPort` | `int` | Required | Port the Load Balancer will balance to |
| `HealthCheck` | [`LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-service-health-check.md) | Required | Service health check |
| `Http` | [`LoadBalancerServiceHttp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https |
| `ListenPort` | `int` | Required | Port the Load Balancer listens on |
| `Protocol` | [`Protocol7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer |
| `Proxyprotocol` | `bool` | Required | Is Proxyprotocol enabled or not |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

LoadBalancerService loadBalancerService = new LoadBalancerService
{
    DestinationPort = 80,
    HealthCheck = new LoadBalancerServiceHealthCheck
    {
        Interval = 15,
        Port = 4711,
        Protocol = Protocol6.Http,
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
    },
    ListenPort = 443,
    Protocol = Protocol7.Https,
    Proxyprotocol = false,
    Http = new LoadBalancerServiceHttp
    {
        Certificates = new List<int>
        {
            180,
        },
        CookieLifetime = 160,
        CookieName = "cookie_name6",
        RedirectHttp = false,
        StickySessions = false,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



