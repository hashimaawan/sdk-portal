# Resources 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlc291cmNlczE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Resources1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AssignedAt` | `*time.Time` | Optional | A time value given in ISO8601 combined date and time format that represents when the project was created. |
| `Links` | [`*models.Links4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/links-4.md) | Optional | The links object contains the `self` object, which contains the resource relationship. |
| `Status` | [`*models.Status14`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-14.md) | Optional | The status of assigning and fetching the resources. |
| `Urn` | `*string` | Optional | The uniform resource name (URN) for the resource in the format do:resource_type:resource_id.<br><br>**Constraints**: *Pattern*: `^do:(dbaas\|domain\|droplet\|floatingip\|loadbalancer\|space\|volume\|kubernetes\|vpc):.*` |
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
    resources1 := models.Resources1{
        AssignedAt:            models.ToPointer(parseTime(time.RFC3339, "2018-09-28T19:26:37Z", func(err error) { log.Fatalln(err) })),
        Links:                 models.ToPointer(models.Links4{
            Self:                  models.ToPointer("self2"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Status:                models.ToPointer(models.Status14_Ok),
        Urn:                   models.ToPointer("do:droplet:13457723"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



