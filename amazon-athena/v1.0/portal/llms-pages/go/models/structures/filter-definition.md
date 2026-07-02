# Filter Definition

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkZpbHRlckRlZmluaXRpb24

A string for searching notebook names.


# Class Name

`FilterDefinition`


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
    filterDefinition := models.FilterDefinition{
        Name:                 models.ToPointer("Name2"),
    }

}
```



