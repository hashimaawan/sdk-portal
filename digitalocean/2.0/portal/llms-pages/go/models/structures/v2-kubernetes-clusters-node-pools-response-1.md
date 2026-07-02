# V2 Kubernetes Clusters Node Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NodePool` | [`*models.NodePool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/node-pool.md) | Optional | - |
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
    v2KubernetesClustersNodePoolsResponse1 := models.V2KubernetesClustersNodePoolsResponse1{
        NodePool:              models.ToPointer(models.NodePool{
            Size:                  "s-1vcpu-2gb",
            AutoScale:             models.ToPointer(true),
            Count:                 3,
            Id:                    models.ToPointer(uuid.MustParse("cdda885e-7663-40c8-bc74-3a036c66545d")),
            Labels:                models.NewOptional[interface{}](nil),
            MaxNodes:              models.ToPointer(6),
            MinNodes:              models.ToPointer(3),
            Name:                  "new-pool",
            Nodes:                 []models.Node{
                models.Node{
                    CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-11-15T16:00:11Z", func(err error) { log.Fatalln(err) })),
                    DropletId:             models.ToPointer(" "),
                    Id:                    models.ToPointer(uuid.MustParse("478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f")),
                    Name:                  models.ToPointer(" "),
                    Status:                models.ToPointer(models.Status10{
                        State:                 models.ToPointer(models.State1_Provisioning),
                    }),
                    UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-11-15T16:00:11Z", func(err error) { log.Fatalln(err) })),
                },
                models.Node{
                    CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-11-15T16:00:11Z", func(err error) { log.Fatalln(err) })),
                    DropletId:             models.ToPointer(" "),
                    Id:                    models.ToPointer(uuid.MustParse("ad12e744-c2a9-473d-8aa9-be5680500eb1")),
                    Name:                  models.ToPointer(" "),
                    Status:                models.ToPointer(models.Status10{
                        State:                 models.ToPointer(models.State1_Provisioning),
                    }),
                    UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-11-15T16:00:11Z", func(err error) { log.Fatalln(err) })),
                },
                models.Node{
                    CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-11-15T16:00:11Z", func(err error) { log.Fatalln(err) })),
                    DropletId:             models.ToPointer(" "),
                    Id:                    models.ToPointer(uuid.MustParse("e46e8d07-f58f-4ff1-9737-97246364400e")),
                    Name:                  models.ToPointer(" "),
                    Status:                models.ToPointer(models.Status10{
                        State:                 models.ToPointer(models.State1_Provisioning),
                    }),
                    UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-11-15T16:00:11Z", func(err error) { log.Fatalln(err) })),
                },
            },
            Tags:                  []string{
                "production",
                "web-team",
                "front-end",
                "k8s",
                "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
                "k8s:worker",
            },
            Taints:                []models.Taint{
            },
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



