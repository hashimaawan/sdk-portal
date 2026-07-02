# V2 Snapshots Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2SnapshotsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Snapshot` | [`*models.Snapshot`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/snapshot.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    v2SnapshotsResponse1 := models.V2SnapshotsResponse1{
        Snapshot:              models.ToPointer(models.Snapshot{
            Id:                    "id8",
            CreatedAt:             parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) }),
            MinDiskSize:           36,
            Name:                  "name8",
            Regions:               []string{
                "regions3",
                "regions4",
                "regions5",
            },
            SizeGigabytes:         float64(140.04),
            ResourceId:            "resource_id4",
            ResourceType:          models.ResourceType1_Droplet,
            Tags:                  []string{
                "tags3",
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



