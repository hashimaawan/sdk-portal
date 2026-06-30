# Playlist Owner Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/java/x-redirect/JTI0bSUyRlBsYXlsaXN0T3duZXJPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`PlaylistOwnerObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExternalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/external-url-object.md) | Optional | Known public external URLs for this user. | ExternalUrlObject getExternalUrls() | setExternalUrls(ExternalUrlObject externalUrls) |
| `Followers` | [`FollowersObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/followers-object.md) | Optional | Information about the followers of this user. | FollowersObject getFollowers() | setFollowers(FollowersObject followers) |
| `Href` | `String` | Optional | A link to the Web API endpoint for this user. | String getHref() | setHref(String href) |
| `Id` | `String` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for this user. | String getId() | setId(String id) |
| `Type` | [`Type3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/enumerations/type-3.md) | Optional | The object type. | Type3 getType() | setType(Type3 type) |
| `Uri` | `String` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for this user. | String getUri() | setUri(String uri) |
| `DisplayName` | `String` | Optional | The name displayed on the user's profile. `null` if not available. | String getDisplayName() | setDisplayName(String displayName) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.ExternalUrlObject;
import com.spotify.api.models.FollowersObject;
import com.spotify.api.models.PlaylistOwnerObject;
import com.spotify.api.models.Type3;
import java.io.IOException;

PlaylistOwnerObject playlistOwnerObject = new PlaylistOwnerObject.Builder()
    .externalUrls(new ExternalUrlObject.Builder()
        .spotify("spotify6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .followers(new FollowersObject.Builder()
        .href("href0")
        .total(82)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .href("href6")
    .id("id4")
    .type(Type3.USER)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



