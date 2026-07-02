# Diagnostic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRpYWdub3N0aWM

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Diagnostic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CheckName` | `*string` | Optional | The clusterlint check that resulted in the diagnostic. |
| `Message` | `*string` | Optional | Feedback about the object for users to fix. |
| `Object` | [`*models.Object`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | Metadata about the Kubernetes API object the diagnostic is reported on. |
| `Severity` | `*string` | Optional | Can be one of error, warning or suggestion. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    diagnostic := models.Diagnostic{
        CheckName:             models.ToPointer("unused-config-map"),
        Message:               models.ToPointer("Unused config map"),
        Object:                models.ToPointer(models.Object{
            Kind:                  models.ToPointer("kind0"),
            Name:                  models.ToPointer("name2"),
            Namespace:             models.ToPointer("namespace0"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Severity:              models.ToPointer("warning"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



