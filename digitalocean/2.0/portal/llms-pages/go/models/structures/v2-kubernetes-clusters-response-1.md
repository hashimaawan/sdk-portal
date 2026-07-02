# V2 Kubernetes Clusters Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2KubernetesClustersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `KubernetesCluster` | [`*models.KubernetesCluster`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/kubernetes-cluster.md) | Optional | - |
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
    v2KubernetesClustersResponse1 := models.V2KubernetesClustersResponse1{
        KubernetesCluster:     models.ToPointer(models.KubernetesCluster{
            AutoUpgrade:           models.ToPointer(false),
            ClusterSubnet:         models.ToPointer("cluster_subnet0"),
            CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            Endpoint:              models.ToPointer("endpoint6"),
            Ha:                    models.ToPointer(false),
            Name:                  "name8",
            NodePools:             []models.NodePool{
                models.NodePool{
                    Size:                  "size6",
                    AutoScale:             models.ToPointer(false),
                    Count:                 206,
                    Id:                    models.ToPointer(uuid.MustParse("000013be-0000-0000-0000-000000000000")),
                    Labels:                models.NewOptional(models.ToPointer(interface{}("[key1, val1][key2, val2]"))),
                    MaxNodes:              models.ToPointer(118),
                    MinNodes:              models.ToPointer(54),
                    Name:                  "name4",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.NodePool{
                    Size:                  "size6",
                    AutoScale:             models.ToPointer(false),
                    Count:                 206,
                    Id:                    models.ToPointer(uuid.MustParse("000013be-0000-0000-0000-000000000000")),
                    Labels:                models.NewOptional(models.ToPointer(interface{}("[key1, val1][key2, val2]"))),
                    MaxNodes:              models.ToPointer(118),
                    MinNodes:              models.ToPointer(54),
                    Name:                  "name4",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Region:                "region4",
            Version:               "version4",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



