# V2 Uptime Checks State Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwU3RhdGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2UptimeChecksStateResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `State` | [`State3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/state-3.md) | Optional | - | State3 getState() | setState(State3 state) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.EuWest;
import com.digitalocean.api.models.PreviousOutage;
import com.digitalocean.api.models.Regions;
import com.digitalocean.api.models.State3;
import com.digitalocean.api.models.Status16;
import com.digitalocean.api.models.V2UptimeChecksStateResponse;
import java.io.IOException;

V2UptimeChecksStateResponse v2UptimeChecksStateResponse = new V2UptimeChecksStateResponse.Builder()
    .state(new State3.Builder()
        .previousOutage(new PreviousOutage.Builder()
            .durationSeconds(16)
            .endedAt("ended_at4")
            .region("region8")
            .startedAt("started_at4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .regions(new Regions.Builder()
            .euWest(new EuWest.Builder()
                .status(Status16.DOWN)
                .statusChangedAt("status_changed_at4")
                .thirtyDayUptimePercentage(227.78D)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .usEast(new EuWest.Builder()
                .status(Status16.DOWN)
                .statusChangedAt("status_changed_at4")
                .thirtyDayUptimePercentage(121.56D)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



