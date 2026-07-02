# Pg Stat Statements Track

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlBnU3RhdFN0YXRlbWVudHNUcmFjaw

Controls which statements are counted. Specify 'top' to track top-level statements (those issued directly by clients), 'all' to also track nested statements (such as statements invoked within functions), or 'none' to disable statement statistics collection. The default value is top.


# Class Name

`PgStatStatementsTrack`


# Fields

| Name |
|  --- |
| `All` |
| `Top` |
| `None` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    pgStatStatementsTrack := models.PgStatStatementsTrack_Top

}
```



