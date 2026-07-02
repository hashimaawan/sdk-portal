# V2 Volumes Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2VolumesSnapshotsResponse`


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
    v2VolumesSnapshotsResponse := models.V2VolumesSnapshotsResponse{
        Snapshot:              models.ToPointer(models.Snapshot{
            Id:                    "8fa70202-873f-11e6-8b68-000f533176b1",
            CreatedAt:             parseTime(time.RFC3339, "2020-09-30T18:56:14Z", func(err error) { log.Fatalln(err) }),
            MinDiskSize:           10,
            Name:                  "big-data-snapshot1475261774",
            Regions:               []string{
                "nyc1",
            },
            SizeGigabytes:         float64(10),
            ResourceId:            "82a48a18-873f-11e6-96bf-000f53315a41",
            ResourceType:          models.ResourceType1_Volume,
            Tags:                  []string{
                "aninterestingtag",
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



