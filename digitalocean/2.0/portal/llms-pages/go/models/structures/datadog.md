# Datadog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRhdGFkb2c

DataDog configuration.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Datadog`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApiKey` | `string` | Required | Datadog API key. |
| `Endpoint` | `*string` | Optional | Datadog HTTP log intake endpoint. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    datadog := models.Datadog{
        ApiKey:                "abcdefghijklmnopqrstuvwxyz0123456789",
        Endpoint:              models.ToPointer("https://mydatadogendpoint.com"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



