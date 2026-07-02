# Type 13

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlR5cGUxMw

Describes the kind of image. It may be one of `snapshot` or `backup`. This specifies whether an image is a user-generated Droplet snapshot or automatically created Droplet backup.


# Class Name

`Type13`


# Fields

| Name |
|  --- |
| `Snapshot` |
| `Backup` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    type13 := models.Type13_Snapshot

}
```



