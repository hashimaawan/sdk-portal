# Effect

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkVmZmVjdA

How the node reacts to pods that it won't tolerate. Available effect values are `NoSchedule`, `PreferNoSchedule`, and `NoExecute`.


# Class Name

`Effect`


# Fields

| Name |
|  --- |
| `Noschedule` |
| `Prefernoschedule` |
| `Noexecute` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    effect := models.Effect_Noschedule

}
```



