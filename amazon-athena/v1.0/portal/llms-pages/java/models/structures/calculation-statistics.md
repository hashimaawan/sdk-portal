# Calculation Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdGlzdGljcw

Contains statistics for a notebook calculation.


# Class Name

`CalculationStatistics`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DpuExecutionInMillis` | `Integer` | Optional | - | Integer getDpuExecutionInMillis() | setDpuExecutionInMillis(Integer dpuExecutionInMillis) |
| `Progress` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getProgress() | setProgress(String progress) |


# Example

```java
import com.amazonaws.useast1.athena.models.CalculationStatistics;

CalculationStatistics calculationStatistics = new CalculationStatistics.Builder()
    .dpuExecutionInMillis(248)
    .progress("Progress8")
    .build();
```



