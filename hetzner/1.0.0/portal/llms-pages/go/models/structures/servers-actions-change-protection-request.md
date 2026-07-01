# Servers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `*bool` | Optional | If true, prevents the Server from being deleted (currently delete and rebuild attribute needs to have the same value) |
| `Rebuild` | `*bool` | Optional | If true, prevents the Server from being rebuilt (currently delete and rebuild attribute needs to have the same value) |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serversActionsChangeProtectionRequest := models.ServersActionsChangeProtectionRequest{
        Delete:               models.ToPointer(true),
        Rebuild:              models.ToPointer(true),
    }

}
```



