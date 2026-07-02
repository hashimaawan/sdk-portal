# V2 Kubernetes Clusters Clusterlint Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2KubernetesClustersClusterlintResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CompletedAt` | `*time.Time` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was completed. |
| `Diagnostics` | [`[]models.Diagnostic`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/diagnostic.md) | Optional | An array of diagnostics reporting potential problems for the given cluster. |
| `RequestedAt` | `*time.Time` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was made. |
| `RunId` | `*string` | Optional | Id of the clusterlint run that can be used later to fetch the diagnostics. |
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
    v2KubernetesClustersClusterlintResponse := models.V2KubernetesClustersClusterlintResponse{
        CompletedAt:           models.ToPointer(parseTime(time.RFC3339, "2019-10-30T05:34:11Z", func(err error) { log.Fatalln(err) })),
        Diagnostics:           []models.Diagnostic{
            models.Diagnostic{
                CheckName:             models.ToPointer("check_name8"),
                Message:               models.ToPointer("message2"),
                Object:                models.ToPointer(models.Object{
                    Kind:                  models.ToPointer("kind0"),
                    Name:                  models.ToPointer("name2"),
                    Namespace:             models.ToPointer("namespace0"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Severity:              models.ToPointer("severity2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Diagnostic{
                CheckName:             models.ToPointer("check_name8"),
                Message:               models.ToPointer("message2"),
                Object:                models.ToPointer(models.Object{
                    Kind:                  models.ToPointer("kind0"),
                    Name:                  models.ToPointer("name2"),
                    Namespace:             models.ToPointer("namespace0"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Severity:              models.ToPointer("severity2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        RequestedAt:           models.ToPointer(parseTime(time.RFC3339, "2019-10-30T05:34:07Z", func(err error) { log.Fatalln(err) })),
        RunId:                 models.ToPointer("50c2f44c-011d-493e-aee5-361a4a0d1844"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



