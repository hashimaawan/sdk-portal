# Rule 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJ1bGUx

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Rule1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ClusterUuid` | `*string` | Optional | A unique ID for the database cluster to which the rule is applied.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` |
| `CreatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall rule was created. |
| `Type` | [`models.Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-7.md) | Required | The type of resource that the firewall rule allows to access the database cluster. |
| `Uuid` | `*string` | Optional | A unique ID for the firewall rule itself.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` |
| `Value` | `string` | Required | The ID of the specific resource, the name of a tag applied to a group of resources, or the IP address that the firewall rule allows to access the database cluster. |
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
    rule1 := models.Rule1{
        ClusterUuid:           models.ToPointer("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30"),
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2019-01-11T18:37:36Z", func(err error) { log.Fatalln(err) })),
        Type:                  models.Type7_Droplet,
        Uuid:                  models.ToPointer("79f26d28-ea8a-41f2-8ad8-8cfcdd020095"),
        Value:                 "ff2a6c52-5a44-4b63-b99c-0e98e7a63d61",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



