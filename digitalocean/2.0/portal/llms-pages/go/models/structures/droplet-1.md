# Droplet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRyb3BsZXQx

An object containing information about a resource scheduled for deletion.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Droplet1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DestroyedAt` | `*time.Time` | Optional | A time value given in ISO8601 combined date and time format indicating when the resource was destroyed if the request was successful. |
| `ErrorMessage` | `*string` | Optional | A string indicating that the resource was not successfully destroyed and providing additional information. |
| `Id` | `*string` | Optional | The unique identifier for the resource scheduled for deletion. |
| `Name` | `*string` | Optional | The name of the resource scheduled for deletion. |
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
    droplet1 := models.Droplet1{
        DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2020-04-01T18:11:49Z", func(err error) { log.Fatalln(err) })),
        ErrorMessage:          models.ToPointer("error_message0"),
        Id:                    models.ToPointer("61486916"),
        Name:                  models.ToPointer("ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



