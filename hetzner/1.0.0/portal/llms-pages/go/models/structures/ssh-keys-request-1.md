# Ssh Keys Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdDE


# Class Name

`SshKeysRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New name Name to set |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    sshKeysRequest1 := models.SshKeysRequest1{
        Labels:               models.ToPointer(interface{}("[labelkey, value]")),
        Name:                 models.ToPointer("My ssh key"),
    }

}
```



