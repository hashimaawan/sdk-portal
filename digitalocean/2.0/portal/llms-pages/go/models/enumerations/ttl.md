# Ttl

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlR0bA

The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.


# Class Name

`Ttl`


# Fields

| Name |
|  --- |
| `Enum60` |
| `Enum600` |
| `Enum3600` |
| `Enum86400` |
| `Enum604800` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    ttl := models.Ttl_Enum60

}
```



