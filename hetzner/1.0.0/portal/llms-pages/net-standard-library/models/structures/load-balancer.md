# Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcg


# Class Name

`LoadBalancer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Algorithm` | [`Algorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/algorithm.md) | Required | Algorithm of the Load Balancer |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Id` | `int` | Required | ID of the Resource |
| `IncludedTraffic` | `int` | Required | Free Traffic for the current billing period in bytes |
| `IngoingTraffic` | `int?` | Required | Inbound Traffic for the current billing period in bytes |
| `Labels` | `Dictionary<string, string>` | Required | User-defined labels (key-value pairs) |
| `LoadBalancerType` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-type.md) | Required | - |
| `Location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/location.md) | Required | - |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `OutgoingTraffic` | `int?` | Required | Outbound Traffic for the current billing period in bytes |
| `PrivateNet` | [`List<PrivateNet>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/private-net.md) | Required | Private networks information |
| `Protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `PublicNet` | [`PublicNet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/public-net.md) | Required | Public network information |
| `Services` | [`List<LoadBalancerService>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-service.md) | Required | List of services that belong to this Load Balancer |
| `Targets` | [`List<LoadBalancerTarget>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-target.md) | Required | List of targets that belong to this Load Balancer |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

LoadBalancer loadBalancer = new LoadBalancer
{
    Algorithm = new Algorithm
    {
        Type = Type28Enum.RoundRobin,
    },
    Created = "2016-01-30T23:55:00+00:00",
    Id = 42,
    IncludedTraffic = 10000,
    IngoingTraffic = 210,
    Labels = new Dictionary<string, string>
    {
        ["key0"] = "labels8",
        ["key1"] = "labels7",
    },
    LoadBalancerType = new LoadBalancerType
    {
        Deprecated = "2016-01-30T23:50:00+00:00",
        Description = "LB11",
        Id = 1,
        MaxAssignedCertificates = 10,
        MaxConnections = 20000,
        MaxServices = 5,
        MaxTargets = 25,
        Name = "lb11",
        Prices = new List<Price>
        {
            new Price
            {
                Location = "fsn1",
                PriceHourly = new PriceHourly
                {
                    Gross = "1.1900000000000000",
                    Net = "1.0000000000",
                },
                PriceMonthly = new PriceMonthly
                {
                    Gross = "1.1900000000000000",
                    Net = "1.0000000000",
                },
            },
        },
    },
    Location = new Location
    {
        City = "Falkenstein",
        Country = "DE",
        Description = "Falkenstein DC Park 1",
        Id = 1,
        Latitude = 50.47612,
        Longitude = 12.370071,
        Name = "fsn1",
        NetworkZone = "eu-central",
    },
    Name = "my-resource",
    OutgoingTraffic = 36,
    PrivateNet = new List<PrivateNet>
    {
        new PrivateNet
        {
            Ip = "10.0.0.2",
            Network = 4711,
        },
    },
    Protection = new Protection
    {
        Delete = false,
    },
    PublicNet = new PublicNet
    {
        Enabled = false,
        Ipv4 = new Ipv4
        {
            DnsPtr = "lb1.example.com",
            Ip = "1.2.3.4",
        },
        Ipv6 = new Ipv6
        {
            DnsPtr = "lb1.example.com",
            Ip = "2001:db8::1",
        },
    },
    Services = new List<LoadBalancerService>
    {
        new LoadBalancerService
        {
            DestinationPort = 80,
            HealthCheck = new LoadBalancerServiceHealthCheck
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
            },
            ListenPort = 443,
            Protocol = Protocol7Enum.Https,
            Proxyprotocol = false,
            Http = new LoadBalancerServiceHTTP
            {
                Certificates = new List<int>
                {
                    180,
                },
                CookieLifetime = 160,
                CookieName = "cookie_name6",
                RedirectHttp = false,
                StickySessions = false,
            },
        },
    },
    Targets = new List<LoadBalancerTarget>
    {
        new LoadBalancerTarget
        {
            Type = Type29Enum.Ip,
            HealthStatus = new List<HealthStatus>
            {
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30Enum.Unknown,
                },
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30Enum.Unknown,
                },
            },
            Ip = new Ip
            {
                Ip = "ip8",
            },
            LabelSelector = new LabelSelector7
            {
                Selector = "selector8",
            },
            Server = new LoadBalancerTargetServer
            {
                Id = 14,
            },
            Targets = new List<Target>
            {
                new Target
                {
                    HealthStatus = new List<HealthStatus>
                    {
                        new HealthStatus
                        {
                            ListenPort = 142,
                            Status = Status30Enum.Unknown,
                        },
                        new HealthStatus
                        {
                            ListenPort = 142,
                            Status = Status30Enum.Unknown,
                        },
                    },
                    Server = new Server11
                    {
                        Id = 14,
                    },
                    Type = "type2",
                    UsePrivateIp = false,
                },
                new Target
                {
                    HealthStatus = new List<HealthStatus>
                    {
                        new HealthStatus
                        {
                            ListenPort = 142,
                            Status = Status30Enum.Unknown,
                        },
                        new HealthStatus
                        {
                            ListenPort = 142,
                            Status = Status30Enum.Unknown,
                        },
                    },
                    Server = new Server11
                    {
                        Id = 14,
                    },
                    Type = "type2",
                    UsePrivateIp = false,
                },
                new Target
                {
                    HealthStatus = new List<HealthStatus>
                    {
                        new HealthStatus
                        {
                            ListenPort = 142,
                            Status = Status30Enum.Unknown,
                        },
                        new HealthStatus
                        {
                            ListenPort = 142,
                            Status = Status30Enum.Unknown,
                        },
                    },
                    Server = new Server11
                    {
                        Id = 14,
                    },
                    Type = "type2",
                    UsePrivateIp = false,
                },
            },
        },
    },
};
```



