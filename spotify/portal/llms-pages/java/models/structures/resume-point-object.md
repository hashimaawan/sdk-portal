# Resume Point Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/java/x-redirect/JTI0bSUyRlJlc3VtZVBvaW50T2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`ResumePointObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FullyPlayed` | `Boolean` | Optional | Whether or not the episode has been fully played by the user. | Boolean getFullyPlayed() | setFullyPlayed(Boolean fullyPlayed) |
| `ResumePositionMs` | `Integer` | Optional | The user's most recent position in the episode in milliseconds. | Integer getResumePositionMs() | setResumePositionMs(Integer resumePositionMs) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.ResumePointObject;
import java.io.IOException;

ResumePointObject resumePointObject = new ResumePointObject.Builder()
    .fullyPlayed(false)
    .resumePositionMs(106)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



