# Get Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlJbnB1dA


# Class Name

`GetNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQueryId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getNamedQueryInput := models.GetNamedQueryInput{
        NamedQueryId:         "NamedQueryId8",
    }

}
```



