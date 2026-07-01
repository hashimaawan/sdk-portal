# Load Balancers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwTWV0cmljcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type object.*


# Class Name

`LoadBalancersMetricsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Metrics` | [`Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/metrics.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Models.Containers;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

LoadBalancersMetricsResponse loadBalancersMetricsResponse = new LoadBalancersMetricsResponse
{
    Metrics = new Metrics
    {
        End = "2017-01-01T23:00:00+00:00",
        Start = "2017-01-01T00:00:00+00:00",
        Step = 60,
        TimeSeries = new Dictionary<string, TimeSeries>
        {
            ["name_of_timeseries"] = new TimeSeries
            {
                Values = new List<List<TimeSeriesValues>>
                {
                    new List<TimeSeriesValues>
                    {
                        TimeSeriesValues.FromPrecision(1435781470.622),
                        TimeSeriesValues.FromString("42"),
                    },
                    new List<TimeSeriesValues>
                    {
                        TimeSeriesValues.FromPrecision(1435781471.622),
                        TimeSeriesValues.FromString("43"),
                    },
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



