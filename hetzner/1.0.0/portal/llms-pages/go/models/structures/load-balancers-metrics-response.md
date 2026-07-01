# Load Balancers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwTWV0cmljcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`LoadBalancersMetricsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Metrics` | [`models.Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/metrics.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    loadBalancersMetricsResponse := models.LoadBalancersMetricsResponse{
        Metrics:               models.Metrics{
            End:                   "2017-01-01T23:00:00+00:00",
            Start:                 "2017-01-01T00:00:00+00:00",
            Step:                  float64(60),
            TimeSeries:            map[string]models.TimeSeries{
                "name_of_timeseries": models.TimeSeries{
                    Values:                [][]models.TimeSeriesValues{
                        {
                            models.TimeSeriesValuesContainer.FromPrecision(float64(1435781470.622)),
                            models.TimeSeriesValuesContainer.FromString("42"),
                        },
                        {
                            models.TimeSeriesValuesContainer.FromPrecision(float64(1435781471.622)),
                            models.TimeSeriesValuesContainer.FromString("43"),
                        },
                    },
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



