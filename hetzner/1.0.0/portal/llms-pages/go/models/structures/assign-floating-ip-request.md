# Assign Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFzc2lnbkZsb2F0aW5nSVBSZXF1ZXN0

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `floating_ip_assigned`        | The floating IP is already assigned                           |

*This model accepts additional fields of type interface{}.*


# Class Name

`AssignFloatingIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Server` | `int` | Required | ID of the Server the Floating IP shall be assigned to |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    assignFloatingIpRequest := models.AssignFloatingIpRequest{
        Server:                42,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



