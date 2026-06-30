# Playlist Tracks Ref Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/java/x-redirect/JTI0bSUyRlBsYXlsaXN0VHJhY2tzUmVmT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`PlaylistTracksRefObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Href` | `String` | Optional | A link to the Web API endpoint where full details of the playlist's tracks can be retrieved. | String getHref() | setHref(String href) |
| `Total` | `Integer` | Optional | Number of tracks in the playlist. | Integer getTotal() | setTotal(Integer total) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.PlaylistTracksRefObject;
import java.io.IOException;

PlaylistTracksRefObject playlistTracksRefObject = new PlaylistTracksRefObject.Builder()
    .href("href6")
    .total(80)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



