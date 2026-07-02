# Get Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cElucHV0


# Class Name

`GetWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getWorkGroupInput := models.GetWorkGroupInput{
        WorkGroup:            "WorkGroup8",
    }

}
```



