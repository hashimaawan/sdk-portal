# Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1ldHJpY3M

*This model accepts additional fields of type object.*


# Class Name

`Metrics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `End` | `string` | Required | End of period of metrics reported (in ISO-8601 format) |
| `Start` | `string` | Required | Start of period of metrics reported (in ISO-8601 format) |
| `Step` | `double` | Required | Resolution of results in seconds. |
| `TimeSeries` | [`Dictionary<string, TimeSeries>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/time-series.md) | Required | Hash with timeseries information, containing the name of timeseries as key |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Models.Containers;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

Metrics metrics = new Metrics
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
};
```



