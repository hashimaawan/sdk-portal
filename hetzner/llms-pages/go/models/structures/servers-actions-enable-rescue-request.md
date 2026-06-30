# Servers Actions Enable Rescue Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXF1ZXN0


# Class Name

`ServersActionsEnableRescueRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SshKeys` | `[]int` | Optional | Array of SSH key IDs which should be injected into the rescue system. |
| `Type` | [`*models.Type65Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-65.md) | Optional | Type of rescue system to boot (default: `linux64`) |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serversActionsEnableRescueRequest := models.ServersActionsEnableRescueRequest{
        SshKeys:              []int{
            2323,
        },
        Type:                 models.ToPointer(models.Type65Enum_LINUX64),
    }

}
```



