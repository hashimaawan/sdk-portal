# V2 Kubernetes Clusters Destroy with Associated Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

An object containing the IDs of resources associated with a Kubernetes cluster.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2KubernetesClustersDestroyWithAssociatedResourcesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancers` | [`[]models.LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated load balancers that can be destroyed along with the cluster. |
| `VolumeSnapshots` | [`[]models.LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated volume snapshots that can be destroyed along with the cluster. |
| `Volumes` | [`[]models.LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated volumes that can be destroyed along with the cluster. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2KubernetesClustersDestroyWithAssociatedResourcesResponse := models.V2KubernetesClustersDestroyWithAssociatedResourcesResponse{
        LoadBalancers:         []models.LoadBalancer{
            models.LoadBalancer{
                Id:                    models.ToPointer("4de7ac8b-495b-4884-9a69-1050c6793cd6"),
                Name:                  models.ToPointer("lb-001"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        VolumeSnapshots:       []models.LoadBalancer{
            models.LoadBalancer{
                Id:                    models.ToPointer("edb0478d-7436-11ea-86e6-0a58ac144b91"),
                Name:                  models.ToPointer("snapshot-001"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Volumes:               []models.LoadBalancer{
            models.LoadBalancer{
                Id:                    models.ToPointer("ba49449a-7435-11ea-b89e-0a58ac14480f"),
                Name:                  models.ToPointer("volume-001"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



