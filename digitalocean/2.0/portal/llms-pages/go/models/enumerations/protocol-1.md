# Protocol 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlByb3RvY29sMQ

The protocol used for health checks sent to the backend Droplets. The possible values are `http`, `https`, or `tcp`.


# Class Name

`Protocol1`


# Fields

| Name |
|  --- |
| `Http` |
| `Https` |
| `Tcp` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    protocol1 := models.Protocol1_Http

}
```



