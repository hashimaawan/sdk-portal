# V2 Projects Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2ProjectsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was created. |
| `Description` | `*string` | Optional | The description of the project. The maximum length is 255 characters.<br><br>**Constraints**: *Maximum Length*: `255` |
| `Environment` | [`*models.Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/environment.md) | Optional | The environment of the project's resources. |
| `Id` | `*uuid.UUID` | Optional, Read-only | The unique universal identifier of this project. |
| `Name` | `*string` | Optional | The human-readable name for the project. The maximum length is 175 characters and the name must be unique.<br><br>**Constraints**: *Maximum Length*: `175` |
| `OwnerId` | `*int` | Optional, Read-only | The integer id of the project owner. |
| `OwnerUuid` | `*string` | Optional, Read-only | The unique universal identifier of the project owner. |
| `Purpose` | `*string` | Optional | The purpose of the project. The maximum length is 255 characters. It can<br>have one of the following values:<br><br>- Just trying out DigitalOcean<br>- Class project / Educational purposes<br>- Website or blog<br>- Web Application<br>- Service or API<br>- Mobile Application<br>- Machine learning / AI / Data processing<br>- IoT<br>- Operational / Developer tooling<br><br>If another value for purpose is specified, for example, "your custom purpose",<br>your purpose will be stored as `Other: your custom purpose`.<br><br>**Constraints**: *Maximum Length*: `255` |
| `UpdatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was updated. |
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
    v2ProjectsRequest := models.V2ProjectsRequest{
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-09-27T20:10:35Z", func(err error) { log.Fatalln(err) })),
        Description:           models.ToPointer("My website API"),
        Environment:           models.ToPointer(models.Environment_Production),
        Id:                    models.ToPointer(uuid.MustParse("4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679")),
        Name:                  models.ToPointer("my-web-api"),
        OwnerId:               models.ToPointer(258992),
        OwnerUuid:             models.ToPointer("99525febec065ca37b2ffe4f852fd2b2581895e7"),
        Purpose:               models.ToPointer("Service or API"),
        UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-09-27T20:10:35Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



