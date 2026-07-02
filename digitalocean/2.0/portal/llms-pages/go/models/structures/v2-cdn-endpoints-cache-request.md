# V2 Cdn Endpoints Cache Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwQ2FjaGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2CdnEndpointsCacheRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Files` | `[]string` | Required | An array of strings containing the path to the content to be purged from the CDN cache. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2CdnEndpointsCacheRequest := models.V2CdnEndpointsCacheRequest{
        Files:                 []string{
            "path/to/image.png",
            "path/to/css/*",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



