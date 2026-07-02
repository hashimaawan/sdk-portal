# V2 Databases Config Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMENvbmZpZyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesConfigRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Config` | [`*models.V2DatabasesConfigRequestConfig`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/v2-databases-config-request-config.md) | Optional | This is a container for any-of cases. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DatabasesConfigRequest := models.V2DatabasesConfigRequest{
        Config:                models.ToPointer(models.V2DatabasesConfigRequestConfigContainer.FromConfig(models.Config{
            BackupHour:                   models.ToPointer(23),
            BackupMinute:                 models.ToPointer(59),
            BinlogRetentionPeriod:        models.ToPointer(float64(600)),
            ConnectTimeout:               models.ToPointer(196),
            DefaultTimeZone:              models.ToPointer("default_time_zone8"),
            AdditionalProperties:         map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



