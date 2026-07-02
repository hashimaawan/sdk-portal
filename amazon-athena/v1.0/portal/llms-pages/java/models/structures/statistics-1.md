# Statistics 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXRpc3RpY3Mx


# Class Name

`Statistics1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DpuExecutionInMillis` | `Integer` | Optional | - | Integer getDpuExecutionInMillis() | setDpuExecutionInMillis(Integer dpuExecutionInMillis) |
| `Progress` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getProgress() | setProgress(String progress) |


# Example

```java
import com.amazonaws.useast1.athena.models.Statistics1;

Statistics1 statistics1 = new Statistics1.Builder()
    .dpuExecutionInMillis(148)
    .progress("Progress4")
    .build();
```



