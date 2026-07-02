# Next Backup Window

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRk5leHRCYWNrdXBXaW5kb3c

The details of the Droplet's backups feature, if backups are configured for the Droplet. This object contains keys for the start and end times of the window during which the backup will start.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`NextBackupWindow`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `End` | `*time.Time` | Optional | A time value given in ISO8601 combined date and time format specifying the end of the Droplet's backup window. |
| `Start` | `*time.Time` | Optional | A time value given in ISO8601 combined date and time format specifying the start of the Droplet's backup window. |
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
    nextBackupWindow := models.NextBackupWindow{
        End:                   models.ToPointer(parseTime(time.RFC3339, "2019-12-04T23:00:00Z", func(err error) { log.Fatalln(err) })),
        Start:                 models.ToPointer(parseTime(time.RFC3339, "2019-12-04T00:00:00Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



