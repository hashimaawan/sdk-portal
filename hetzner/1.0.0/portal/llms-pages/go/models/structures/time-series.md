# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM

*This model accepts additional fields of type interface{}.*


# Class Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Values` | [`[][]models.TimeSeriesValues`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/oneof-anyof-definitions/time-series-values.md) | Required | This is 2d Array of a container for one-of cases. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    timeSeries := models.TimeSeries{
        Values:                [][]models.TimeSeriesValues{
            {
                models.TimeSeriesValuesContainer.FromPrecision(float64(138.94)),
                models.TimeSeriesValuesContainer.FromPrecision(float64(138.95)),
            },
            {
                models.TimeSeriesValuesContainer.FromPrecision(float64(138.94)),
                models.TimeSeriesValuesContainer.FromPrecision(float64(138.95)),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



