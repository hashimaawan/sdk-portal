# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM


# Class Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Values` | [`List<List<TimeSeriesValues>>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/oneof-anyof-definitions/time-series-values.md) | Required | This is 2d List of a container for one-of cases. | List<List<TimeSeriesValues>> getValues() | setValues(List<List<TimeSeriesValues>> values) |


# Example

```java
import cloud.hetzner.api.models.TimeSeries;
import cloud.hetzner.api.models.containers.TimeSeriesValues;
import java.util.Arrays;

TimeSeries timeSeries = new TimeSeries.Builder(
    Arrays.asList(
        Arrays.asList(
            TimeSeriesValues.fromPrecision(
                138.94D
            ),
            TimeSeriesValues.fromPrecision(
                138.95D
            )
        ),
        Arrays.asList(
            TimeSeriesValues.fromPrecision(
                138.94D
            ),
            TimeSeriesValues.fromPrecision(
                138.95D
            )
        )
    )
)
.build();
```



