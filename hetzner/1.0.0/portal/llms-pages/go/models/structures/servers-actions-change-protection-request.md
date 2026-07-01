# Servers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`ServersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `*bool` | Optional | If true, prevents the Server from being deleted (currently delete and rebuild attribute needs to have the same value) |
| `Rebuild` | `*bool` | Optional | If true, prevents the Server from being rebuilt (currently delete and rebuild attribute needs to have the same value) |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serversActionsChangeProtectionRequest := models.ServersActionsChangeProtectionRequest{
        Delete:                models.ToPointer(true),
        Rebuild:               models.ToPointer(true),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



