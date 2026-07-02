# V2 Apps Components Logs Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBDb21wb25lbnRzJTI1MjBMb2dzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsComponentsLogsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HistoricUrls` | `List<String>` | Optional | - | List<String> getHistoricUrls() | setHistoricUrls(List<String> historicUrls) |
| `LiveUrl` | `String` | Optional | A URL of the real-time live logs. This URL may use either the `https://` or `wss://` protocols and will keep pushing live logs as they become available. | String getLiveUrl() | setLiveUrl(String liveUrl) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2AppsComponentsLogsResponse;
import java.io.IOException;
import java.util.Arrays;

V2AppsComponentsLogsResponse v2AppsComponentsLogsResponse = new V2AppsComponentsLogsResponse.Builder()
    .historicUrls(Arrays.asList(
        "historic_urls9",
        "historic_urls0",
        "historic_urls1"
    ))
    .liveUrl("ws://logs/build")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



