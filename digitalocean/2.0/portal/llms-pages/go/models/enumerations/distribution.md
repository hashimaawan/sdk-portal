# Distribution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRpc3RyaWJ1dGlvbg

The name of a custom image's distribution. Currently, the valid values are  `Arch Linux`, `CentOS`, `CoreOS`, `Debian`, `Fedora`, `Fedora Atomic`,  `FreeBSD`, `Gentoo`, `openSUSE`, `RancherOS`, `Rocky Linux`, `Ubuntu`, and `Unknown`.  Any other value will be accepted but ignored, and `Unknown` will be used in its place.


# Class Name

`Distribution`


# Fields

| Name |
|  --- |
| `EnumArchLinux` |
| `Centos` |
| `Coreos` |
| `Debian` |
| `Fedora` |
| `EnumFedoraAtomic` |
| `Freebsd` |
| `Gentoo` |
| `Opensuse` |
| `Rancheros` |
| `EnumRockyLinux` |
| `Ubuntu` |
| `Unknown` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    distribution := models.Distribution_EnumFedoraAtomic

}
```



