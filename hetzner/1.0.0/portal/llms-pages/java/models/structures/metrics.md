# Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRk1ldHJpY3M


# Class Name

`Metrics`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `End` | `String` | Required | End of period of metrics reported (in ISO-8601 format) | String getEnd() | setEnd(String end) |
| `Start` | `String` | Required | Start of period of metrics reported (in ISO-8601 format) | String getStart() | setStart(String start) |
| `Step` | `double` | Required | Resolution of results in seconds. | double getStep() | setStep(double step) |
| `TimeSeries` | [`Map<String, TimeSeries>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/time-series.md) | Required | Hash with timeseries information, containing the name of timeseries as key | Map<String, TimeSeries> getTimeSeries() | setTimeSeries(Map<String, TimeSeries> timeSeries) |


# Example

```java
import cloud.hetzner.api.models.Metrics;
import cloud.hetzner.api.models.TimeSeries;
import cloud.hetzner.api.models.containers.TimeSeriesValues;
import java.util.Arrays;
import java.util.LinkedHashMap;

Metrics metrics = new Metrics.Builder(
    "2017-01-01T23:00:00+00:00",
    "2017-01-01T00:00:00+00:00",
    60D,
    new LinkedHashMap<String, TimeSeries>() {{
        put("name_of_timeseries", new TimeSeries.Builder(
            Arrays.asList(
                Arrays.asList(
                    TimeSeriesValues.fromPrecision(
                        1435781470.622D
                    ),
                    TimeSeriesValues.fromString(
                        "42"
                    )
                ),
                Arrays.asList(
                    TimeSeriesValues.fromPrecision(
                        1435781471.622D
                    ),
                    TimeSeriesValues.fromString(
                        "43"
                    )
                )
            )
        )
        .build());
    }}
)
.build();
```



