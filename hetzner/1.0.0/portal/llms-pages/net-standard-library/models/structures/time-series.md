# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM


# Class Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Values` | [`List<List<TimeSeriesValues>>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/oneof-anyof-definitions/time-series-values.md) | Required | This is 2d List of a container for one-of cases. |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using HetznerCloudAPI.Standard.Models.Containers;
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
};
```



