# Previous Outage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlByZXZpb3VzT3V0YWdl

*This model accepts additional fields of type Object.*


# Class Name

`PreviousOutage`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DurationSeconds` | `Integer` | Optional | - | Integer getDurationSeconds() | setDurationSeconds(Integer durationSeconds) |
| `EndedAt` | `String` | Optional | - | String getEndedAt() | setEndedAt(String endedAt) |
| `Region` | `String` | Optional | - | String getRegion() | setRegion(String region) |
| `StartedAt` | `String` | Optional | - | String getStartedAt() | setStartedAt(String startedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.PreviousOutage;
import java.io.IOException;

PreviousOutage previousOutage = new PreviousOutage.Builder()
    .durationSeconds(120)
    .endedAt("2022-03-17T18:06:55Z")
    .region("us_east")
    .startedAt("2022-03-17T18:04:55Z")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



