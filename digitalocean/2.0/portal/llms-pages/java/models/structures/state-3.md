# State 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXRlMw

*This model accepts additional fields of type Object.*


# Class Name

`State3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PreviousOutage` | [`PreviousOutage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/previous-outage.md) | Optional | - | PreviousOutage getPreviousOutage() | setPreviousOutage(PreviousOutage previousOutage) |
| `Regions` | [`Regions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/regions.md) | Optional | A map of region to regional state | Regions getRegions() | setRegions(Regions regions) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.EuWest;
import com.digitalocean.api.models.PreviousOutage;
import com.digitalocean.api.models.Regions;
import com.digitalocean.api.models.State3;
import com.digitalocean.api.models.Status16;
import java.io.IOException;

State3 state3 = new State3.Builder()
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
    .build();
```



