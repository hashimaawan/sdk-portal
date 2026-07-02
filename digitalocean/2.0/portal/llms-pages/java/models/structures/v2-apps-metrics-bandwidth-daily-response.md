# V2 Apps Metrics Bandwidth Daily Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsMetricsBandwidthDailyResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AppBandwidthUsage` | [`List<AppBandwidthUsage>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/app-bandwidth-usage.md) | Optional | A list of bandwidth usage details by app. | List<AppBandwidthUsage> getAppBandwidthUsage() | setAppBandwidthUsage(List<AppBandwidthUsage> appBandwidthUsage) |
| `Date` | `LocalDateTime` | Optional | The date for the metrics data. | LocalDateTime getDate() | setDate(LocalDateTime date) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.AppBandwidthUsage;
import com.digitalocean.api.models.V2AppsMetricsBandwidthDailyResponse;
import java.io.IOException;
import java.util.Arrays;

V2AppsMetricsBandwidthDailyResponse v2AppsMetricsBandwidthDailyResponse = new V2AppsMetricsBandwidthDailyResponse.Builder()
    .appBandwidthUsage(Arrays.asList(
        new AppBandwidthUsage.Builder()
            .appId("app_id4")
            .bandwidthBytes("bandwidth_bytes6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new AppBandwidthUsage.Builder()
            .appId("app_id4")
            .bandwidthBytes("bandwidth_bytes6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .date(DateTimeHelper.fromRfc8601DateTime("2023-01-17T00:00:00Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



