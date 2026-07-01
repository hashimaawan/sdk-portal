# Load Balancers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2Uy

*This model accepts additional fields of type object.*


# Class Name

`LoadBalancersResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancer` | [`LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

LoadBalancersResponse2 loadBalancersResponse2 = new LoadBalancersResponse2
{
    LoadBalancer = new LoadBalancer
    {
        Algorithm = new Algorithm
        {
            Type = Type28.RoundRobin,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Created = "2016-01-30T23:55:00+00:00",
        Id = 42,
        IncludedTraffic = 10000,
        IngoingTraffic = 216,
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels2",
            ["key1"] = "labels1",
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
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    PriceMonthly = new PriceMonthly
                    {
                        Gross = "1.1900000000000000",
                        Net = "1.0000000000",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Name = "my-resource",
        OutgoingTraffic = 42,
        PrivateNet = new List<PrivateNet>
        {
            new PrivateNet
            {
                Ip = "10.0.0.2",
                Network = 4711,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Protection = new Protection
        {
            Delete = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        PublicNet = new PublicNet
        {
            Enabled = false,
            Ipv4 = new Ipv4
            {
                DnsPtr = "lb1.example.com",
                Ip = "1.2.3.4",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Ipv6 = new Ipv6
            {
                DnsPtr = "lb1.example.com",
                Ip = "2001:db8::1",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
            },
        },
        Targets = new List<LoadBalancerTarget>
        {
            new LoadBalancerTarget
            {
                Type = Type29.Ip,
                HealthStatus = new List<HealthStatus>
                {
                    new HealthStatus
                    {
                        ListenPort = 142,
                        Status = Status30.Unknown,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new HealthStatus
                    {
                        ListenPort = 142,
                        Status = Status30.Unknown,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Ip = new Ip
                {
                    Ip = "ip8",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                LabelSelector = new LabelSelector7
                {
                    Selector = "selector8",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Server = new LoadBalancerTargetServer
                {
                    Id = 14,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
                                Status = Status30.Unknown,
                                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                            },
                            new HealthStatus
                            {
                                ListenPort = 142,
                                Status = Status30.Unknown,
                                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                            },
                        },
                        Server = new Server11
                        {
                            Id = 14,
                            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                        },
                        Type = "type2",
                        UsePrivateIp = false,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new Target
                    {
                        HealthStatus = new List<HealthStatus>
                        {
                            new HealthStatus
                            {
                                ListenPort = 142,
                                Status = Status30.Unknown,
                                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                            },
                            new HealthStatus
                            {
                                ListenPort = 142,
                                Status = Status30.Unknown,
                                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                            },
                        },
                        Server = new Server11
                        {
                            Id = 14,
                            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                        },
                        Type = "type2",
                        UsePrivateIp = false,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new Target
                    {
                        HealthStatus = new List<HealthStatus>
                        {
                            new HealthStatus
                            {
                                ListenPort = 142,
                                Status = Status30.Unknown,
                                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                            },
                            new HealthStatus
                            {
                                ListenPort = 142,
                                Status = Status30.Unknown,
                                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                            },
                        },
                        Server = new Server11
                        {
                            Id = 14,
                            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                        },
                        Type = "type2",
                        UsePrivateIp = false,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



