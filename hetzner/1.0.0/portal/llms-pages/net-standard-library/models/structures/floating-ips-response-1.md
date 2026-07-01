# Floating Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type object.*


# Class Name

`FloatingIpsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action.md) | Optional | - |
| `FloatingIp` | [`FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/floating-ip.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

FloatingIpsResponse1 floatingIpsResponse1 = new FloatingIpsResponse1
{
    FloatingIp = new FloatingIp
    {
        Blocked = false,
        Created = "2016-01-30T23:55:00+00:00",
        Description = "this describes my resource",
        DnsPtr = new List<DnsPtr>
        {
            new DnsPtr
            {
                DnsPtrProp = "server.example.com",
                Ip = "2001:db8::1",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        HomeLocation = new HomeLocation
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
        Id = 42,
        Ip = "131.232.99.1",
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels4",
            ["key1"] = "labels3",
            ["key2"] = "labels2",
        },
        Name = "my-resource",
        Protection = new Protection
        {
            Delete = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Server = 42,
        Type = Type16.Ipv4,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Action = new Action
    {
        Command = "command6",
        Error = new Error
        {
            Code = "code2",
            Message = "message4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Finished = "finished0",
        Id = 238,
        Progress = 143.26,
        Resources = new List<Resource>
        {
            new Resource
            {
                Id = 198,
                Type = "type0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Resource
            {
                Id = 198,
                Type = "type0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Resource
            {
                Id = 198,
                Type = "type0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Started = "started8",
        Status = Status.Running,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



