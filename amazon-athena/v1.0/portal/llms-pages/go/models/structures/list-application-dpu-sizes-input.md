# List Application DPU Sizes Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzSW5wdXQ


# Class Name

`ListApplicationDPUSizesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listApplicationDPUSizesInput := models.ListApplicationDPUSizesInput{
        MaxResults:           models.ToPointer(100),
        NextToken:            models.ToPointer("NextToken8"),
    }

}
```



