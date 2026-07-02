# Garbage Collection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkdhcmJhZ2VDb2xsZWN0aW9u

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`GarbageCollection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BlobsDeleted` | `*int` | Optional | The number of blobs deleted as a result of this garbage collection. |
| `CreatedAt` | `*time.Time` | Optional | The time the garbage collection was created. |
| `FreedBytes` | `*int` | Optional | The number of bytes freed as a result of this garbage collection. |
| `RegistryName` | `*string` | Optional | The name of the container registry. |
| `Status` | [`*models.Status15`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-15.md) | Optional | The current status of this garbage collection. |
| `UpdatedAt` | `*time.Time` | Optional | The time the garbage collection was last updated. |
| `Uuid` | `*string` | Optional | A string specifying the UUID of the garbage collection. |
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
    garbageCollection := models.GarbageCollection{
        BlobsDeleted:          models.ToPointer(42),
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-10-30T21:03:24Z", func(err error) { log.Fatalln(err) })),
        FreedBytes:            models.ToPointer(667),
        RegistryName:          models.ToPointer("example"),
        Status:                models.ToPointer(models.Status15_Requested),
        UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-10-30T21:03:44Z", func(err error) { log.Fatalln(err) })),
        Uuid:                  models.ToPointer("eff0feee-49c7-4e8f-ba5c-a320c109c8a8"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



