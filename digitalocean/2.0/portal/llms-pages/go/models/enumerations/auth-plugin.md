# Auth Plugin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkF1dGhQbHVnaW4

A string specifying the authentication method to be used for connections
to the MySQL user account. The valid values are `mysql_native_password`
or `caching_sha2_password`. If excluded when creating a new user, the
default for the version of MySQL in use will be used. As of MySQL 8.0, the
default is `caching_sha2_password`.


# Class Name

`AuthPlugin`


# Fields

| Name |
|  --- |
| `MysqlNativePassword` |
| `CachingSha2Password` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    authPlugin := models.AuthPlugin_MysqlNativePassword

}
```



