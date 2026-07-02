# Size 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlNpemUy

This field has been replaced by the `size_unit` field for all regions except in AMS2, NYC2, and SFO1. Each available load balancer size now equates to the load balancer having a set number of nodes.

* `lb-small` = 1 node
* `lb-medium` = 3 nodes
* `lb-large` = 6 nodes

You can resize load balancers after creation up to once per hour. You cannot resize a load balancer within the first hour of its creation.


# Class Name

`Size2`


# Fields

| Name |
|  --- |
| `Lbsmall` |
| `Lbmedium` |
| `Lblarge` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    size2 := models.Size2_Lbmedium

}
```



