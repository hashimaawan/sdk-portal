# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`AssignPrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AssigneeId` | `int` | Required | ID of a resource of type `assignee_type` |
| `AssigneeType` | `string` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `"server"` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    assignPrimaryIpRequest := models.AssignPrimaryIpRequest{
        AssigneeId:            4711,
        AssigneeType:          "server",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



