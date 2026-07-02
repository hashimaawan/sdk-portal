# V2 Kubernetes Clusters Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing the IDs of resources to be destroyed along with their associated with a Kubernetes cluster.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancers` | `[]string` | Optional | A list of IDs for associated load balancers to destroy along with the cluster. |
| `VolumeSnapshots` | `[]string` | Optional | A list of IDs for associated volume snapshots to destroy along with the cluster. |
| `Volumes` | `[]string` | Optional | A list of IDs for associated volumes to destroy along with the cluster. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest := models.V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest{
        LoadBalancers:         []string{
            "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        },
        VolumeSnapshots:       []string{
            "edb0478d-7436-11ea-86e6-0a58ac144b91",
        },
        Volumes:               []string{
            "ba49449a-7435-11ea-b89e-0a58ac14480f",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



