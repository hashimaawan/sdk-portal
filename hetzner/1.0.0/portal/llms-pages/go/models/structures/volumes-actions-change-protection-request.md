# Volumes Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA


# Class Name

`VolumesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `*bool` | Optional | If true, prevents the Volume from being deleted |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    volumesActionsChangeProtectionRequest := models.VolumesActionsChangeProtectionRequest{
        Delete:               models.ToPointer(true),
    }

}
```



