# Type 12

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlR5cGUxMg

The type of action to initiate for the Droplet.


# Class Name

`Type12`


# Fields

| Name |
|  --- |
| `EnableBackups` |
| `DisableBackups` |
| `Reboot` |
| `PowerCycle` |
| `Shutdown` |
| `PowerOff` |
| `PowerOn` |
| `Restore` |
| `PasswordReset` |
| `Resize` |
| `Rebuild` |
| `Rename` |
| `ChangeKernel` |
| `EnableIpv6` |
| `Snapshot` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    type12 := models.Type12_Reboot

}
```



