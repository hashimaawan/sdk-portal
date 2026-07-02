# Kubernetes Cluster

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVy

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`KubernetesCluster`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutoUpgrade` | `bool?` | Optional | A boolean value indicating whether the cluster will be automatically upgraded to new patch releases during its maintenance window.<br><br>**Default**: `false` |
| `ClusterSubnet` | `string` | Optional, Read-only | The range of IP addresses in the overlay network of the Kubernetes cluster in CIDR notation. |
| `CreatedAt` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the Kubernetes cluster was created. |
| `Endpoint` | `string` | Optional, Read-only | The base URL of the API server on the Kubernetes master node. |
| `Ha` | `bool?` | Optional | A boolean value indicating whether the control plane is run in a highly available configuration in the cluster. Highly available control planes incur less downtime. The property cannot be disabled.<br><br>**Default**: `false` |
| `Id` | `Guid?` | Optional, Read-only | A unique ID that can be used to identify and reference a Kubernetes cluster. |
| `Ipv4` | `string` | Optional, Read-only | The public IPv4 address of the Kubernetes master node. This will not be set if high availability is configured on the cluster (v1.21+) |
| `MaintenancePolicy` | [`MaintenancePolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/maintenance-policy.md) | Optional | An object specifying the maintenance window policy for the Kubernetes cluster. |
| `Name` | `string` | Required | A human-readable name for a Kubernetes cluster. |
| `NodePools` | [`List<NodePool>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/node-pool.md) | Required | An object specifying the details of the worker nodes available to the Kubernetes cluster. |
| `Region` | `string` | Required | The slug identifier for the region where the Kubernetes cluster is located. |
| `RegistryEnabled` | `bool?` | Optional, Read-only | A read-only boolean value indicating if a container registry is integrated with the cluster. |
| `ServiceSubnet` | `string` | Optional, Read-only | The range of assignable IP addresses for services running in the Kubernetes cluster in CIDR notation. |
| `Status` | [`Status11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/status-11.md) | Optional, Read-only | An object containing a `state` attribute whose value is set to a string indicating the current status of the cluster. |
| `SurgeUpgrade` | `bool?` | Optional | A boolean value indicating whether surge upgrade is enabled/disabled for the cluster. Surge upgrade makes cluster upgrades fast and reliable by bringing up new nodes before destroying the outdated nodes.<br><br>**Default**: `false` |
| `Tags` | `List<string>` | Optional | An array of tags applied to the Kubernetes cluster. All clusters are automatically tagged `k8s` and `k8s:$K8S_CLUSTER_ID`. |
| `UpdatedAt` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the Kubernetes cluster was last updated. |
| `Version` | `string` | Required | The slug identifier for the version of Kubernetes used for the cluster. If set to a minor version (e.g. "1.14"), the latest version within it will be used (e.g. "1.14.6-do.1"); if set to "latest", the latest published version will be used. See the `/v2/kubernetes/options` endpoint to find all currently available versions. |
| `VpcUuid` | `Guid?` | Optional | A string specifying the UUID of the VPC to which the Kubernetes cluster is assigned. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

KubernetesCluster kubernetesCluster = new KubernetesCluster
{
    Name = "prod-cluster-01",
    NodePools = new List<NodePool>
    {
        new NodePool
        {
            Size = "s-1vcpu-2gb",
            Count = 3,
            Name = "frontend-pool",
            AutoScale = true,
            Id = new Guid("cdda885e-7663-40c8-bc74-3a036c66545d"),
            Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            MaxNodes = 6,
            MinNodes = 3,
            Tags = new List<string>
            {
                "k8s",
                "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
                "k8s-worker",
                "production",
                "web-team",
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Region = "nyc1",
    Version = "1.18.6-do.0",
    AutoUpgrade = true,
    ClusterSubnet = "10.244.0.0/16",
    CreatedAt = DateTime.ParseExact("2018-11-15T16:00:11Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Endpoint = "https://bd5f5959-5e1e-4205-a714-a914373942af.k8s.ondigitalocean.com",
    Ha = true,
    Id = new Guid("bd5f5959-5e1e-4205-a714-a914373942af"),
    Ipv4 = "68.183.121.157",
    RegistryEnabled = true,
    ServiceSubnet = "10.245.0.0/16",
    SurgeUpgrade = true,
    Tags = new List<string>
    {
        "k8s",
        "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
        "production",
        "web-team",
    },
    UpdatedAt = DateTime.ParseExact("2018-11-15T16:00:11Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    VpcUuid = new Guid("c33931f2-a26a-4e61-b85c-4e95a2ec431b"),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



