# App Bandwidth Usage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkFwcEJhbmR3aWR0aFVzYWdl

Bandwidth usage for an app.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`AppBandwidthUsage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AppId` | `*string` | Optional | The ID of the app. |
| `BandwidthBytes` | `*string` | Optional | The used bandwidth amount in bytes. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    appBandwidthUsage := models.AppBandwidthUsage{
        AppId:                 models.ToPointer("4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf"),
        BandwidthBytes:        models.ToPointer("513668"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



