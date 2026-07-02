# Delete Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkRlbGV0ZU5hbWVkUXVlcnlJbnB1dA


# Class Name

`DeleteNamedQueryInput`


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
    deleteNamedQueryInput := models.DeleteNamedQueryInput{
        NamedQueryId:         "NamedQueryId4",
    }

}
```



