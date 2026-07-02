# Backup 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkJhY2t1cDE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Backup1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int` | Required | The unique identifier for the snapshot or backup. |
| `CreatedAt` | `time.Time` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. |
| `MinDiskSize` | `int` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. |
| `Name` | `string` | Required | A human-readable name for the snapshot. |
| `Regions` | `[]string` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. |
| `SizeGigabytes` | `float64` | Required | The billable size of the snapshot in gigabytes. |
| `Type` | [`models.Type13`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-13.md) | Required | Describes the kind of image. It may be one of `snapshot` or `backup`. This specifies whether an image is a user-generated Droplet snapshot or automatically created Droplet backup. |
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
    backup1 := models.Backup1{
        Id:                    6372321,
        CreatedAt:             parseTime(time.RFC3339, "2020-07-28T16:47:44Z", func(err error) { log.Fatalln(err) }),
        MinDiskSize:           25,
        Name:                  "web-01-1595954862243",
        Regions:               []string{
            "nyc3",
            "sfo3",
        },
        SizeGigabytes:         float64(2.34),
        Type:                  models.Type13_Snapshot,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



