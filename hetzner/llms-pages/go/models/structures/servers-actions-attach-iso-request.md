# Servers Actions Attach Iso Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEF0dGFjaCUyNTIwSXNvJTI1MjBSZXF1ZXN0


# Class Name

`ServersActionsAttachIsoRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Iso` | `string` | Required | ID or name of ISO to attach to the Server as listed in GET `/isos` |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serversActionsAttachIsoRequest := models.ServersActionsAttachIsoRequest{
        Iso:                  "FreeBSD-11.0-RELEASE-amd64-dvd1",
    }

}
```



