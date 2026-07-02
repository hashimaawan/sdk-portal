# Type 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlR5cGU5

Describes the kind of image. It may be one of `base`, `snapshot`, `backup`, `custom`, or `admin`. Respectively, this specifies whether an image is a DigitalOcean base OS image, user-generated Droplet snapshot, automatically created Droplet backup, user-provided virtual machine image, or an image used for DigitalOcean managed resources (e.g. DOKS worker nodes).


# Class Name

`Type9`


# Fields

| Name |
|  --- |
| `Base` |
| `Snapshot` |
| `Backup` |
| `Custom` |
| `Admin` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    type9 := models.Type9_Custom

}
```



