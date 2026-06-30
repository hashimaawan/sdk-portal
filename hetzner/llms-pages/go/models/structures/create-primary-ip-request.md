# Create Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlcXVlc3Q


# Class Name

`CreatePrimaryIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AssigneeId` | `*int` | Optional | ID of the resource the Primary IP should be assigned to. Omitted if it should not be assigned. |
| `AssigneeType` | `string` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `"server"` |
| `AutoDelete` | `*bool` | Optional | Delete the Primary IP when the Server it is assigned to is deleted. If omitted defaults to `false`. |
| `Datacenter` | `*string` | Optional | ID or name of Datacenter the Primary IP will be bound to. Needs to be omitted if `assignee_id` is passed. |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | - |
| `Type` | [`models.Type51Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-51.md) | Required | Primary IP type |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createPrimaryIPRequest := models.CreatePrimaryIPRequest{
        AssigneeId:           models.ToPointer(17),
        AssigneeType:         "server",
        AutoDelete:           models.ToPointer(false),
        Datacenter:           models.ToPointer("fsn1-dc8"),
        Labels:               models.ToPointer(interface{}("[labelkey, value]")),
        Name:                 "my-ip",
        Type:                 models.Type51Enum_IPV4,
    }

}
```



