# V2 Apps Components Logs Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBDb21wb25lbnRzJTI1MjBMb2dzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2AppsComponentsLogsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `HistoricUrls` | `[]string` | Optional | - |
| `LiveUrl` | `*string` | Optional | A URL of the real-time live logs. This URL may use either the `https://` or `wss://` protocols and will keep pushing live logs as they become available. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2AppsComponentsLogsResponse := models.V2AppsComponentsLogsResponse{
        HistoricUrls:          []string{
            "historic_urls9",
            "historic_urls0",
            "historic_urls1",
        },
        LiveUrl:               models.ToPointer("ws://logs/build"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



