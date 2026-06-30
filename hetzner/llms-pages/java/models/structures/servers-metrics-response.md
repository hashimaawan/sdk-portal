# Servers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyME1ldHJpY3MlMjUyMFJlc3BvbnNl


# Class Name

`ServersMetricsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Metrics` | [`Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/metrics.md) | Required | - | Metrics getMetrics() | setMetrics(Metrics metrics) |


# Example

```java
import cloud.hetzner.api.models.Metrics;
import cloud.hetzner.api.models.ServersMetricsResponse;
import cloud.hetzner.api.models.TimeSeries;
import cloud.hetzner.api.models.containers.TimeSeriesValues;
import java.util.Arrays;
import java.util.LinkedHashMap;

ServersMetricsResponse serversMetricsResponse = new ServersMetricsResponse.Builder(
    new Metrics.Builder(
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
    .build()
)
.build();
```



