# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM

*This model accepts additional fields of type object.*


# Class Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Values` | [`List<List<TimeSeriesValues>>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/oneof-anyof-definitions/time-series-values.md) | Required | This is 2d List of a container for one-of cases. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Models.Containers;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

TimeSeries timeSeries = new TimeSeries
{
    Values = new List<List<TimeSeriesValues>>
    {
        new List<TimeSeriesValues>
        {
            TimeSeriesValues.FromPrecision(138.94),
            TimeSeriesValues.FromPrecision(138.95),
        },
        new List<TimeSeriesValues>
        {
            TimeSeriesValues.FromPrecision(138.94),
            TimeSeriesValues.FromPrecision(138.95),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



