# Eu West

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkV1V2VzdA

*This model accepts additional fields of type Object.*


# Class Name

`EuWest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Status` | [`Status16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-16.md) | Optional | - | Status16 getStatus() | setStatus(Status16 status) |
| `StatusChangedAt` | `String` | Optional | - | String getStatusChangedAt() | setStatusChangedAt(String statusChangedAt) |
| `ThirtyDayUptimePercentage` | `Double` | Optional | - | Double getThirtyDayUptimePercentage() | setThirtyDayUptimePercentage(Double thirtyDayUptimePercentage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.EuWest;
import com.digitalocean.api.models.Status16;
import java.io.IOException;

EuWest euWest = new EuWest.Builder()
    .status(Status16.UP)
    .statusChangedAt("2022-03-17T22:28:51Z")
    .thirtyDayUptimePercentage(97.99D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



