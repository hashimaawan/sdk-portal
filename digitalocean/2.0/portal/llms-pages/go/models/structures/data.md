# Data

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRhdGE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Data`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Result` | [`[]models.Result`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/result.md) | Required | Result of query. |
| `ResultType` | `string` | Required, Constant | **Value**: `"matrix"` |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    data := models.Data{
        Result:                []models.Result{
            models.Result{
                Metric:                map[string]string{
                    "host_id": "19201920",
                },
                Values:                [][]models.ResultValues{
                    {
                        models.ResultValuesContainer.FromNumber(1435781430),
                        models.ResultValuesContainer.FromString("1"),
                    },
                    {
                        models.ResultValuesContainer.FromNumber(1435781445),
                        models.ResultValuesContainer.FromString("1"),
                    },
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        ResultType:            "matrix",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



