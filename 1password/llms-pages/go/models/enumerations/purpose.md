# Purpose

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRlB1cnBvc2U

Some item types, Login and Password, have fields used for autofill. This property indicates that purpose and is required for some item types.


# Class Name

`Purpose`


# Fields

| Name |
|  --- |
| `Username` |
| `Password` |
| `Notes` |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    purpose := models.Purpose_Password

}
```



