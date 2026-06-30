# Artist Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/java/x-redirect/JTI0bSUyRkFydGlzdE9iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`ArtistObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExternalUrls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/structures/external-url-object.md) | Optional | Known external URLs for this artist. | ExternalUrlObject getExternalUrls() | setExternalUrls(ExternalUrlObject externalUrls) |
| `Followers` | [`FollowersObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/structures/followers-object.md) | Optional | Information about the followers of the artist. | FollowersObject getFollowers() | setFollowers(FollowersObject followers) |
| `Genres` | `List<String>` | Optional | A list of the genres the artist is associated with. If not yet classified, the array is empty. | List<String> getGenres() | setGenres(List<String> genres) |
| `Href` | `String` | Optional | A link to the Web API endpoint providing full details of the artist. | String getHref() | setHref(String href) |
| `Id` | `String` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the artist. | String getId() | setId(String id) |
| `Images` | [`List<ImageObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/structures/image-object.md) | Optional | Images of the artist in various sizes, widest first. | List<ImageObject> getImages() | setImages(List<ImageObject> images) |
| `Name` | `String` | Optional | The name of the artist. | String getName() | setName(String name) |
| `Popularity` | `Integer` | Optional | The popularity of the artist. The value will be between 0 and 100, with 100 being the most popular. The artist's popularity is calculated from the popularity of all the artist's tracks. | Integer getPopularity() | setPopularity(Integer popularity) |
| `Type` | [`Type`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/enumerations/type.md) | Optional | The object type. | Type getType() | setType(Type type) |
| `Uri` | `String` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the artist. | String getUri() | setUri(String uri) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.ArtistObject;
import com.spotify.api.models.ExternalUrlObject;
import com.spotify.api.models.FollowersObject;
import java.io.IOException;
import java.util.Arrays;

ArtistObject artistObject = new ArtistObject.Builder()
    .externalUrls(new ExternalUrlObject.Builder()
        .spotify("spotify6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .followers(new FollowersObject.Builder()
        .href("href0")
        .total(82)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .genres(Arrays.asList(
        "Prog rock",
        "Grunge"
    ))
    .href("href8")
    .id("id6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



