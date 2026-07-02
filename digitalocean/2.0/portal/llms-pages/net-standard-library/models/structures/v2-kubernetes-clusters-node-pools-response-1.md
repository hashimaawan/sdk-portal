# V2 Kubernetes Clusters Node Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NodePool` | [`NodePool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/node-pool.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2KubernetesClustersNodePoolsResponse1 v2KubernetesClustersNodePoolsResponse1 = new V2KubernetesClustersNodePoolsResponse1
{
    NodePool = new NodePool
    {
        Size = "s-1vcpu-2gb",
        Count = 3,
        Name = "new-pool",
        AutoScale = true,
        Id = new Guid("cdda885e-7663-40c8-bc74-3a036c66545d"),
        Labels = null,
        MaxNodes = 6,
        MinNodes = 3,
        Nodes = new List<Node>
        {
            new Node
            {
                CreatedAt = DateTime.ParseExact("2018-11-15T16:00:11Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                DropletId = " ",
                Id = new Guid("478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f"),
                Name = " ",
                Status = new Status10
                {
                    State = State1.Provisioning,
                },
                UpdatedAt = DateTime.ParseExact("2018-11-15T16:00:11Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
            },
            new Node
            {
                CreatedAt = DateTime.ParseExact("2018-11-15T16:00:11Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                DropletId = " ",
                Id = new Guid("ad12e744-c2a9-473d-8aa9-be5680500eb1"),
                Name = " ",
                Status = new Status10
                {
                    State = State1.Provisioning,
                },
                UpdatedAt = DateTime.ParseExact("2018-11-15T16:00:11Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
            },
            new Node
            {
                CreatedAt = DateTime.ParseExact("2018-11-15T16:00:11Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                DropletId = " ",
                Id = new Guid("e46e8d07-f58f-4ff1-9737-97246364400e"),
                Name = " ",
                Status = new Status10
                {
                    State = State1.Provisioning,
                },
                UpdatedAt = DateTime.ParseExact("2018-11-15T16:00:11Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
            },
        },
        Tags = new List<string>
        {
            "production",
            "web-team",
            "front-end",
            "k8s",
            "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
            "k8s:worker",
        },
        Taints = new List<Taint>
        {

        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



