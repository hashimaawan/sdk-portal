# V2 Uptime Checks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2UptimeChecksResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Check` | [`*models.Check`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/check.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
    "github.com/google/uuid"
)

func main() {
    v2UptimeChecksResponse1 := models.V2UptimeChecksResponse1{
        Check:                 models.ToPointer(models.Check{
            Id:                    models.ToPointer(uuid.MustParse("00000c0a-0000-0000-0000-000000000000")),
            Enabled:               models.ToPointer(false),
            Name:                  models.ToPointer("name2"),
            Regions:               []models.Region8{
                models.Region8_SeAsia,
            },
            Target:                models.ToPointer("target0"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



