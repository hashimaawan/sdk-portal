# Renewal

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlJlbmV3YWw

Status of the renewal process of the Certificate.


# Class Name

`RenewalEnum`


# Fields

| Name |
|  --- |
| `SCHEDULED` |
| `PENDING` |
| `FAILED` |
| `UNAVAILABLE` |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    renewal := models.RenewalEnum_FAILED

}
```



