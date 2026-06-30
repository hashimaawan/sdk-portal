# Playlist Snapshot Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/java/x-redirect/JTI0bSUyRlBsYXlsaXN0U25hcHNob3RJZA

*This model accepts additional fields of type Object.*


# Class Name

`PlaylistSnapshotId`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SnapshotId` | `String` | Optional | - | String getSnapshotId() | setSnapshotId(String snapshotId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.PlaylistSnapshotId;
import java.io.IOException;

PlaylistSnapshotId playlistSnapshotId = new PlaylistSnapshotId.Builder()
    .snapshotId("abc")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



