# External Url Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/java/x-redirect/JTI0bSUyRkV4dGVybmFsVXJsT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`ExternalUrlObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Spotify` | `String` | Optional | The [Spotify URL](/documentation/web-api/concepts/spotify-uris-ids) for the object. | String getSpotify() | setSpotify(String spotify) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.ExternalUrlObject;
import java.io.IOException;

ExternalUrlObject externalUrlObject = new ExternalUrlObject.Builder()
    .spotify("spotify0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



