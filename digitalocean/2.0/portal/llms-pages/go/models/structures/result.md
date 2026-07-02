# Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Result`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Metric` | `map[string]string` | Required | An object containing the metric labels. |
| `Values` | [`[][]models.ResultValues`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/result-values.md) | Required | This is 2d Array of a container for one-of cases. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    result := models.Result{
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
    }

}
```



