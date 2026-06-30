# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM


# Class Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Values` | [`[][]models.TimeSeriesValues`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/oneof-anyof-definitions/time-series-values.md) | Required | This is 2d Array of a container for one-of cases. |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    timeSeries := models.TimeSeries{
        Values:               [][]models.TimeSeriesValues{
            {
                models.TimeSeriesValuesContainer.FromPrecision(float64(138.94)),
                models.TimeSeriesValuesContainer.FromPrecision(float64(138.95)),
            },
            {
                models.TimeSeriesValuesContainer.FromPrecision(float64(138.94)),
                models.TimeSeriesValuesContainer.FromPrecision(float64(138.95)),
            },
        },
    }

}
```



