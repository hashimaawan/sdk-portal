# Ssh Keys Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdA


# Class Name

`SshKeysRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the SSH key |
| `PublicKey` | `string` | Required | Public key |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    sshKeysRequest := models.SshKeysRequest{
        Labels:               models.ToPointer(interface{}("[key1, val1][key2, val2]")),
        Name:                 "My ssh key",
        PublicKey:            "ssh-rsa AAAjjk76kgf...Xt",
    }

}
```



