# V2 Kubernetes Clusters Node Pools Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutoScale` | `bool?` | Optional | A boolean value indicating whether auto-scaling is enabled for this node pool. |
| `Count` | `int?` | Optional | The number of Droplet instances in the node pool. |
| `Id` | `Guid?` | Optional, Read-only | A unique ID that can be used to identify and reference a specific node pool. |
| `Labels` | [`object`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | An object containing a set of Kubernetes labels. The keys and are values are both user-defined. |
| `MaxNodes` | `int?` | Optional | The maximum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. |
| `MinNodes` | `int?` | Optional | The minimum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. |
| `Name` | `string` | Optional | A human-readable name for the node pool. |
| `Nodes` | [`List<Node>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/node.md) | Optional, Read-only | An object specifying the details of a specific worker node in a node pool. |
| `Tags` | `List<string>` | Optional | An array containing the tags applied to the node pool. All node pools are automatically tagged `k8s`, `k8s-worker`, and `k8s:$K8S_CLUSTER_ID`. |
| `Taints` | [`List<Taint>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/taint.md) | Optional | An array of taints to apply to all nodes in a pool. Taints will automatically be applied to all existing nodes and any subsequent nodes added to the pool. When a taint is removed, it is removed from all nodes in the pool. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2KubernetesClustersNodePoolsRequest v2KubernetesClustersNodePoolsRequest = new V2KubernetesClustersNodePoolsRequest
{
    AutoScale = true,
    Count = 3,
    Id = new Guid("cdda885e-7663-40c8-bc74-3a036c66545d"),
    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    MaxNodes = 6,
    MinNodes = 3,
    Name = "frontend-pool",
    Tags = new List<string>
    {
        "k8s",
        "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
        "k8s-worker",
        "production",
        "web-team",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



