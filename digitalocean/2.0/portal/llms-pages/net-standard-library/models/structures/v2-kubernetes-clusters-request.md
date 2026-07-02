# V2 Kubernetes Clusters Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2KubernetesClustersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutoUpgrade` | `bool?` | Optional | A boolean value indicating whether the cluster will be automatically upgraded to new patch releases during its maintenance window.<br><br>**Default**: `false` |
| `Ha` | `bool?` | Optional | A boolean value indicating whether the control plane is run in a highly available configuration in the cluster. Highly available control planes incur less downtime. The property cannot be disabled.<br><br>**Default**: `false` |
| `MaintenancePolicy` | [`MaintenancePolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/maintenance-policy.md) | Optional | An object specifying the maintenance window policy for the Kubernetes cluster. |
| `Name` | `string` | Required | A human-readable name for a Kubernetes cluster. |
| `SurgeUpgrade` | `bool?` | Optional | A boolean value indicating whether surge upgrade is enabled/disabled for the cluster. Surge upgrade makes cluster upgrades fast and reliable by bringing up new nodes before destroying the outdated nodes.<br><br>**Default**: `false` |
| `Tags` | `List<string>` | Optional | An array of tags applied to the Kubernetes cluster. All clusters are automatically tagged `k8s` and `k8s:$K8S_CLUSTER_ID`. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2KubernetesClustersRequest v2KubernetesClustersRequest = new V2KubernetesClustersRequest
{
    Name = "prod-cluster-01",
    AutoUpgrade = true,
    Ha = true,
    MaintenancePolicy = new MaintenancePolicy
    {
        Day = Day.Any,
        Duration = "duration4",
        StartTime = "start_time2",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    SurgeUpgrade = true,
    Tags = new List<string>
    {
        "k8s",
        "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
        "production",
        "web-team",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



