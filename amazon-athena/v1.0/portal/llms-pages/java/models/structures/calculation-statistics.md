# Calculation Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdGlzdGljcw

Contains statistics for a notebook calculation.

*This model accepts additional fields of type Object.*


# Class Name

`CalculationStatistics`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DpuExecutionInMillis` | `Integer` | Optional | - | Integer getDpuExecutionInMillis() | setDpuExecutionInMillis(Integer dpuExecutionInMillis) |
| `Progress` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getProgress() | setProgress(String progress) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.CalculationStatistics;
import java.io.IOException;

CalculationStatistics calculationStatistics = new CalculationStatistics.Builder()
    .dpuExecutionInMillis(248)
    .progress("Progress8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



