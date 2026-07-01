# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Automount` | `*bool` | Optional | Auto-mount the Volume after attaching it |
| `Server` | `int` | Required | ID of the Server the Volume will be attached to |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    attachVolumeRequest := models.AttachVolumeRequest{
        Automount:             models.ToPointer(false),
        Server:                43,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



