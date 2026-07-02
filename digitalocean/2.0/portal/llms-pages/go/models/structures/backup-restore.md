# Backup Restore

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkJhY2t1cFJlc3RvcmU

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`BackupRestore`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BackupCreatedAt` | `*time.Time` | Optional | The timestamp of an existing database cluster backup in ISO8601 combined date and time format. The most recent backup will be used if excluded. |
| `DatabaseName` | `string` | Required | The name of an existing database cluster from which the backup will be restored. |
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
    backupRestore := models.BackupRestore{
        BackupCreatedAt:       models.ToPointer(parseTime(time.RFC3339, "2019-01-31T19:25:22Z", func(err error) { log.Fatalln(err) })),
        DatabaseName:          "backend",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



