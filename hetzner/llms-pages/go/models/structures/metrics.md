# Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRk1ldHJpY3M


# Class Name

`Metrics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `End` | `string` | Required | End of period of metrics reported (in ISO-8601 format) |
| `Start` | `string` | Required | Start of period of metrics reported (in ISO-8601 format) |
| `Step` | `float64` | Required | Resolution of results in seconds. |
| `TimeSeries` | [`map[string]models.TimeSeries`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/time-series.md) | Required | Hash with timeseries information, containing the name of timeseries as key |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    metrics := models.Metrics{
        End:                  "2017-01-01T23:00:00+00:00",
        Start:                "2017-01-01T00:00:00+00:00",
        Step:                 float64(60),
        TimeSeries:           map[string]models.TimeSeries{
            "name_of_timeseries": models.TimeSeries{
                Values:               [][]models.TimeSeriesValues{
                    {
                        models.TimeSeriesValuesContainer.FromPrecision(float64(1435781470.622)),
                        models.TimeSeriesValuesContainer.FromString("42"),
                    },
                    {
                        models.TimeSeriesValuesContainer.FromPrecision(float64(1435781471.622)),
                        models.TimeSeriesValuesContainer.FromString("43"),
                    },
                },
            },
        },
    }

}
```



