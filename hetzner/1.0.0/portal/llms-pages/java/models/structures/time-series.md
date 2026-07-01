# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM

*This model accepts additional fields of type Object.*


# Class Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Values` | [`List<List<TimeSeriesValues>>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/oneof-anyof-definitions/time-series-values.md) | Required | This is 2d List of a container for one-of cases. | List<List<TimeSeriesValues>> getValues() | setValues(List<List<TimeSeriesValues>> values) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.TimeSeries;
import cloud.hetzner.api.models.containers.TimeSeriesValues;
import java.io.IOException;
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
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



