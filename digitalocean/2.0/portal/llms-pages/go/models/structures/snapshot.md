# Snapshot

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlNuYXBzaG90

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Snapshot`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Required | The unique identifier for the snapshot. |
| `CreatedAt` | `time.Time` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. |
| `MinDiskSize` | `int` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. |
| `Name` | `string` | Required | A human-readable name for the snapshot. |
| `Regions` | `[]string` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. |
| `SizeGigabytes` | `float64` | Required | The billable size of the snapshot in gigabytes. |
| `ResourceId` | `string` | Required | The unique identifier for the resource that the snapshot originated from. |
| `ResourceType` | [`models.ResourceType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/resource-type-1.md) | Required | The type of resource that the snapshot originated from. |
| `Tags` | `[]string` | Required | An array of Tags the snapshot has been tagged with. |
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
    snapshot := models.Snapshot{
        Id:                    "6372321",
        CreatedAt:             parseTime(time.RFC3339, "2020-07-28T16:47:44Z", func(err error) { log.Fatalln(err) }),
        MinDiskSize:           25,
        Name:                  "web-01-1595954862243",
        Regions:               []string{
            "nyc3",
            "sfo3",
        },
        SizeGigabytes:         float64(2.34),
        ResourceId:            "200776916",
        ResourceType:          models.ResourceType1_Droplet,
        Tags:                  []string{
            "web",
            "env:prod",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



