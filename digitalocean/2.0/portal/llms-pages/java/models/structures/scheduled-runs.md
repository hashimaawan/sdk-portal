# Scheduled Runs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlNjaGVkdWxlZFJ1bnM

*This model accepts additional fields of type Object.*


# Class Name

`ScheduledRuns`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LastRunAt` | `String` | Optional | Indicates last run time. null value indicates trigger not run yet. | String getLastRunAt() | setLastRunAt(String lastRunAt) |
| `NextRunAt` | `String` | Optional | Indicates next run time. null value indicates trigger will not run. | String getNextRunAt() | setNextRunAt(String nextRunAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.ScheduledRuns;
import java.io.IOException;

ScheduledRuns scheduledRuns = new ScheduledRuns.Builder()
    .lastRunAt("2022-11-11T04:16:45Z")
    .nextRunAt("2022-11-11T04:16:45Z")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



