# Log Error Verbosity

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkxvZ0Vycm9yVmVyYm9zaXR5

Controls the amount of detail written in the server log for each message that is logged.


# Class Name

`LogErrorVerbosity`


# Fields

| Name |
|  --- |
| `Terse` |
| `Default` |
| `Verbose` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    logErrorVerbosity := models.LogErrorVerbosity_Default

}
```



