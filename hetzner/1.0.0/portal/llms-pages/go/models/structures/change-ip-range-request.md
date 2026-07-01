# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0

*This model accepts additional fields of type interface{}.*


# Class Name

`ChangeIpRangeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpRange` | `string` | Required | The new prefix for the whole Network |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    changeIpRangeRequest := models.ChangeIpRangeRequest{
        IpRange:               "10.0.0.0/12",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



