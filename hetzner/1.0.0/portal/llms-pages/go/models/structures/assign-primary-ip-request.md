# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q


# Class Name

`AssignPrimaryIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AssigneeId` | `int` | Required | ID of a resource of type `assignee_type` |
| `AssigneeType` | `string` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `"server"` |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    assignPrimaryIPRequest := models.AssignPrimaryIPRequest{
        AssigneeId:           4711,
        AssigneeType:         "server",
    }

}
```



