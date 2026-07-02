# Kubernetes Cluster

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVy

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`KubernetesCluster`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutoUpgrade` | `*bool` | Optional | A boolean value indicating whether the cluster will be automatically upgraded to new patch releases during its maintenance window.<br><br>**Default**: `false` |
| `ClusterSubnet` | `*string` | Optional, Read-only | The range of IP addresses in the overlay network of the Kubernetes cluster in CIDR notation. |
| `CreatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the Kubernetes cluster was created. |
| `Endpoint` | `*string` | Optional, Read-only | The base URL of the API server on the Kubernetes master node. |
| `Ha` | `*bool` | Optional | A boolean value indicating whether the control plane is run in a highly available configuration in the cluster. Highly available control planes incur less downtime. The property cannot be disabled.<br><br>**Default**: `false` |
| `Id` | `*uuid.UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a Kubernetes cluster. |
| `Ipv4` | `*string` | Optional, Read-only | The public IPv4 address of the Kubernetes master node. This will not be set if high availability is configured on the cluster (v1.21+) |
| `MaintenancePolicy` | [`models.Optional[models.MaintenancePolicy]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/maintenance-policy.md) | Optional | An object specifying the maintenance window policy for the Kubernetes cluster. |
| `Name` | `string` | Required | A human-readable name for a Kubernetes cluster. |
| `NodePools` | [`[]models.NodePool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/node-pool.md) | Required | An object specifying the details of the worker nodes available to the Kubernetes cluster. |
| `Region` | `string` | Required | The slug identifier for the region where the Kubernetes cluster is located. |
| `RegistryEnabled` | `*bool` | Optional, Read-only | A read-only boolean value indicating if a container registry is integrated with the cluster. |
| `ServiceSubnet` | `*string` | Optional, Read-only | The range of assignable IP addresses for services running in the Kubernetes cluster in CIDR notation. |
| `Status` | [`*models.Status11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/status-11.md) | Optional, Read-only | An object containing a `state` attribute whose value is set to a string indicating the current status of the cluster. |
| `SurgeUpgrade` | `*bool` | Optional | A boolean value indicating whether surge upgrade is enabled/disabled for the cluster. Surge upgrade makes cluster upgrades fast and reliable by bringing up new nodes before destroying the outdated nodes.<br><br>**Default**: `false` |
| `Tags` | `[]string` | Optional | An array of tags applied to the Kubernetes cluster. All clusters are automatically tagged `k8s` and `k8s:$K8S_CLUSTER_ID`. |
| `UpdatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the Kubernetes cluster was last updated. |
| `Version` | `string` | Required | The slug identifier for the version of Kubernetes used for the cluster. If set to a minor version (e.g. "1.14"), the latest version within it will be used (e.g. "1.14.6-do.1"); if set to "latest", the latest published version will be used. See the `/v2/kubernetes/options` endpoint to find all currently available versions. |
| `VpcUuid` | `*uuid.UUID` | Optional | A string specifying the UUID of the VPC to which the Kubernetes cluster is assigned. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
    "github.com/google/uuid"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    kubernetesCluster := models.KubernetesCluster{
        AutoUpgrade:           models.ToPointer(true),
        ClusterSubnet:         models.ToPointer("10.244.0.0/16"),
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-11-15T16:00:11Z", func(err error) { log.Fatalln(err) })),
        Endpoint:              models.ToPointer("https://bd5f5959-5e1e-4205-a714-a914373942af.k8s.ondigitalocean.com"),
        Ha:                    models.ToPointer(true),
        Id:                    models.ToPointer(uuid.MustParse("bd5f5959-5e1e-4205-a714-a914373942af")),
        Ipv4:                  models.ToPointer("68.183.121.157"),
        Name:                  "prod-cluster-01",
        NodePools:             []models.NodePool{
            models.NodePool{
                Size:                  "s-1vcpu-2gb",
                AutoScale:             models.ToPointer(true),
                Count:                 3,
                Id:                    models.ToPointer(uuid.MustParse("cdda885e-7663-40c8-bc74-3a036c66545d")),
                Labels:                models.NewOptional(models.ToPointer(interface{}("[key1, val1][key2, val2]"))),
                MaxNodes:              models.ToPointer(6),
                MinNodes:              models.ToPointer(3),
                Name:                  "frontend-pool",
                Tags:                  []string{
                    "k8s",
                    "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
                    "k8s-worker",
                    "production",
                    "web-team",
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Region:                "nyc1",
        RegistryEnabled:       models.ToPointer(true),
        ServiceSubnet:         models.ToPointer("10.245.0.0/16"),
        SurgeUpgrade:          models.ToPointer(true),
        Tags:                  []string{
            "k8s",
            "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
            "production",
            "web-team",
        },
        UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-11-15T16:00:11Z", func(err error) { log.Fatalln(err) })),
        Version:               "1.18.6-do.0",
        VpcUuid:               models.ToPointer(uuid.MustParse("c33931f2-a26a-4e61-b85c-4e95a2ec431b")),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



