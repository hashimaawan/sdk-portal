# Servers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyME1ldHJpY3MlMjUyMFJlc3BvbnNl


# Class Name

`ServersMetricsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Metrics` | [`Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/metrics.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using HetznerCloudAPI.Standard.Models.Containers;
using System.Collections.Generic;

ServersMetricsResponse serversMetricsResponse = new ServersMetricsResponse
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
            },
        },
    },
};
```



