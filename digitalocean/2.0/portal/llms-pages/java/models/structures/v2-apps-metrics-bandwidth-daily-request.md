# V2 Apps Metrics Bandwidth Daily Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsMetricsBandwidthDailyRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AppIds` | `List<String>` | Required | A list of app IDs to query bandwidth metrics for.<br><br>**Constraints**: *Maximum Items*: `100` | List<String> getAppIds() | setAppIds(List<String> appIds) |
| `Date` | `LocalDateTime` | Optional | Optional day to query. Only the date component of the timestamp will be considered. Default: yesterday. | LocalDateTime getDate() | setDate(LocalDateTime date) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.V2AppsMetricsBandwidthDailyRequest;
import java.io.IOException;
import java.util.Arrays;

V2AppsMetricsBandwidthDailyRequest v2AppsMetricsBandwidthDailyRequest = new V2AppsMetricsBandwidthDailyRequest.Builder(
    Arrays.asList(
        "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        "c2a93513-8d9b-4223-9d61-5e7272c81cf5"
    )
)
.date(DateTimeHelper.fromRfc8601DateTime("2023-01-17T00:00:00Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



