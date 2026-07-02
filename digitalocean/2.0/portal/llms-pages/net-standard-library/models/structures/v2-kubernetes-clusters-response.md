# V2 Kubernetes Clusters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2KubernetesClustersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `KubernetesClusters` | [`List<KubernetesCluster>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/kubernetes-cluster.md) | Optional | - |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/links.md) | Optional | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2KubernetesClustersResponse v2KubernetesClustersResponse = new V2KubernetesClustersResponse
{
    Meta = new Meta
    {
        Total = 1,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    KubernetesClusters = new List<KubernetesCluster>
    {
        new KubernetesCluster
        {
            Name = "name2",
            NodePools = new List<NodePool>
            {
                new NodePool
                {
                    Size = "size6",
                    Count = 206,
                    Name = "name4",
                    AutoScale = false,
                    Id = new Guid("000013be-0000-0000-0000-000000000000"),
                    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    MaxNodes = 118,
                    MinNodes = 54,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new NodePool
                {
                    Size = "size6",
                    Count = 206,
                    Name = "name4",
                    AutoScale = false,
                    Id = new Guid("000013be-0000-0000-0000-000000000000"),
                    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    MaxNodes = 118,
                    MinNodes = 54,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new NodePool
                {
                    Size = "size6",
                    Count = 206,
                    Name = "name4",
                    AutoScale = false,
                    Id = new Guid("000013be-0000-0000-0000-000000000000"),
                    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    MaxNodes = 118,
                    MinNodes = 54,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Region = "region8",
            Version = "version8",
            AutoUpgrade = false,
            ClusterSubnet = "cluster_subnet4",
            CreatedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Endpoint = "endpoint0",
            Ha = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new KubernetesCluster
        {
            Name = "name2",
            NodePools = new List<NodePool>
            {
                new NodePool
                {
                    Size = "size6",
                    Count = 206,
                    Name = "name4",
                    AutoScale = false,
                    Id = new Guid("000013be-0000-0000-0000-000000000000"),
                    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    MaxNodes = 118,
                    MinNodes = 54,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new NodePool
                {
                    Size = "size6",
                    Count = 206,
                    Name = "name4",
                    AutoScale = false,
                    Id = new Guid("000013be-0000-0000-0000-000000000000"),
                    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    MaxNodes = 118,
                    MinNodes = 54,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new NodePool
                {
                    Size = "size6",
                    Count = 206,
                    Name = "name4",
                    AutoScale = false,
                    Id = new Guid("000013be-0000-0000-0000-000000000000"),
                    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    MaxNodes = 118,
                    MinNodes = 54,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Region = "region8",
            Version = "version8",
            AutoUpgrade = false,
            ClusterSubnet = "cluster_subnet4",
            CreatedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Endpoint = "endpoint0",
            Ha = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new KubernetesCluster
        {
            Name = "name2",
            NodePools = new List<NodePool>
            {
                new NodePool
                {
                    Size = "size6",
                    Count = 206,
                    Name = "name4",
                    AutoScale = false,
                    Id = new Guid("000013be-0000-0000-0000-000000000000"),
                    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    MaxNodes = 118,
                    MinNodes = 54,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new NodePool
                {
                    Size = "size6",
                    Count = 206,
                    Name = "name4",
                    AutoScale = false,
                    Id = new Guid("000013be-0000-0000-0000-000000000000"),
                    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    MaxNodes = 118,
                    MinNodes = 54,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new NodePool
                {
                    Size = "size6",
                    Count = 206,
                    Name = "name4",
                    AutoScale = false,
                    Id = new Guid("000013be-0000-0000-0000-000000000000"),
                    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    MaxNodes = 118,
                    MinNodes = 54,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Region = "region8",
            Version = "version8",
            AutoUpgrade = false,
            ClusterSubnet = "cluster_subnet4",
            CreatedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Endpoint = "endpoint0",
            Ha = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Links = new Links
    {
        Pages = LinksPages.FromPages(
            new Pages
            {
                Last = "last6",
                Next = "next2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            }
        ),
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



