# V2 Databases Backups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMEJhY2t1cHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesBackupsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Backups` | [`[]models.Backup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/backup.md) | Required | - |
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
    v2DatabasesBackupsResponse := models.V2DatabasesBackupsResponse{
        Backups:               []models.Backup{
            models.Backup{
                CreatedAt:             parseTime(time.RFC3339, "2019-01-31T19:25:22Z", func(err error) { log.Fatalln(err) }),
                SizeGigabytes:         float64(0.03364864),
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



