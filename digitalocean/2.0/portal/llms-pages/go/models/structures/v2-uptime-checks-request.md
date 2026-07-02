# V2 Uptime Checks Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2UptimeChecksRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Enabled` | `*bool` | Optional | A boolean value indicating whether the check is enabled/disabled.<br><br>**Default**: `true` |
| `Name` | `*string` | Optional | A human-friendly display name. |
| `Regions` | [`[]models.Region8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/region-8.md) | Optional | An array containing the selected regions to perform healthchecks from. |
| `Target` | `*string` | Optional | The endpoint to perform healthchecks on. |
| `Type` | [`*models.Type19`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-19.md) | Optional | The type of health check to perform. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2UptimeChecksRequest := models.V2UptimeChecksRequest{
        Enabled:               models.ToPointer(true),
        Name:                  models.ToPointer("Landing page check"),
        Regions:               []models.Region8{
            models.Region8_UsEast,
            models.Region8_EuWest,
        },
        Target:                models.ToPointer("https://www.landingpage.com"),
        Type:                  models.ToPointer(models.Type19_Https),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



