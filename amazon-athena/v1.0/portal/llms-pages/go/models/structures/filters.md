# Filters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkZpbHRlcnM


# Class Name

`Filters`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    filters := models.Filters{
        Name:                 models.ToPointer("Name0"),
    }

}
```



