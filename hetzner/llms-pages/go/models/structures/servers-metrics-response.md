# Servers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyME1ldHJpY3MlMjUyMFJlc3BvbnNl


# Class Name

`ServersMetricsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Metrics` | [`models.Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/metrics.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serversMetricsResponse := models.ServersMetricsResponse{
        Metrics:              models.Metrics{
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
        },
    }

}
```



