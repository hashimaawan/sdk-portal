# Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaW1hcnlJUFJlc3BvbnNl

*This model accepts additional fields of type object.*


# Class Name

`PrimaryIpResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PrimaryIp` | [`PrimaryIp1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/primary-ip-1.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

PrimaryIpResponse primaryIpResponse = new PrimaryIpResponse
{
    PrimaryIp = new PrimaryIp1
    {
        AssigneeId = 17,
        AssigneeType = "server",
        AutoDelete = true,
        Blocked = false,
        Created = "2016-01-30T23:55:00+00:00",
        Datacenter = new Datacenter2
        {
            Description = "Falkenstein DC Park 8",
            Id = 42,
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
            Name = "fsn1-dc8",
            ServerTypes = new ServerTypes
            {
                Available = new List<double>
                {
                    1,
                    2,
                    3,
                },
                AvailableForMigration = new List<double>
                {
                    1,
                    2,
                    3,
                },
                Supported = new List<double>
                {
                    1,
                    2,
                    3,
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        DnsPtr = new List<DnsPtr>
        {
            new DnsPtr
            {
                DnsPtrProp = "server.example.com",
                Ip = "2001:db8::1",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Id = 42,
        Ip = "131.232.99.1",
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels2",
            ["key1"] = "labels1",
        },
        Name = "my-resource",
        Protection = new Protection
        {
            Delete = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Type = Type50.Ipv4,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



