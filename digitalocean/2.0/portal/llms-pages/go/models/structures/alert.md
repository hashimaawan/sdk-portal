# Alert

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkFsZXJ0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Alert`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Disabled` | `*bool` | Optional | Is the alert disabled? |
| `Operator` | [`*models.Operator`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/operator.md) | Optional | **Default**: `"UNSPECIFIED_OPERATOR"` |
| `Rule` | [`*models.Rule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/rule.md) | Optional | **Default**: `"UNSPECIFIED_RULE"` |
| `Value` | `*float64` | Optional | Threshold value for alert |
| `Window` | [`*models.Window`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/window.md) | Optional | **Default**: `"UNSPECIFIED_WINDOW"` |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    alert := models.Alert{
        Disabled:              models.ToPointer(false),
        Operator:              models.ToPointer(models.Operator_GreaterThan),
        Rule:                  models.ToPointer(models.Rule_CpuUtilization),
        Value:                 models.ToPointer(float64(2.32)),
        Window:                models.ToPointer(models.Window_FiveMinutes),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



