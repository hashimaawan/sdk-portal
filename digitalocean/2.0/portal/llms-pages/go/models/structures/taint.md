# Taint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlRhaW50

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Taint`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Effect` | [`*models.Effect`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/effect.md) | Optional | How the node reacts to pods that it won't tolerate. Available effect values are `NoSchedule`, `PreferNoSchedule`, and `NoExecute`. |
| `Key` | `*string` | Optional | An arbitrary string. The `key` and `value` fields of the `taint` object form a key-value pair. For example, if the value of the `key` field is "special" and the value of the `value` field is "gpu", the key value pair would be `special=gpu`. |
| `Value` | `*string` | Optional | An arbitrary string. The `key` and `value` fields of the `taint` object form a key-value pair. For example, if the value of the `key` field is "special" and the value of the `value` field is "gpu", the key value pair would be `special=gpu`. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    taint := models.Taint{
        Effect:                models.ToPointer(models.Effect_Noschedule),
        Key:                   models.ToPointer("priority"),
        Value:                 models.ToPointer("high"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



