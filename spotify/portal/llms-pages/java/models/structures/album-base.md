# Album Base

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/java/x-redirect/JTI0bSUyRkFsYnVtQmFzZQ

*This model accepts additional fields of type Object.*


# Class Name

`AlbumBase`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AlbumType` | [`AlbumType`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/enumerations/album-type.md) | Required | The type of the album. | AlbumType getAlbumType() | setAlbumType(AlbumType albumType) |
| `TotalTracks` | `int` | Required | The number of tracks in the album. | int getTotalTracks() | setTotalTracks(int totalTracks) |
| `AvailableMarkets` | `List<String>` | Required | The markets in which the album is available: [ISO 3166-1 alpha-2 country codes](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). _**NOTE**: an album is considered available in a market when at least 1 of its tracks is available in that market._ | List<String> getAvailableMarkets() | setAvailableMarkets(List<String> availableMarkets) |
| `ExternalUrls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/structures/external-url-object.md) | Required | Known external URLs for this album. | ExternalUrlObject getExternalUrls() | setExternalUrls(ExternalUrlObject externalUrls) |
| `Href` | `String` | Required | A link to the Web API endpoint providing full details of the album. | String getHref() | setHref(String href) |
| `Id` | `String` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the album. | String getId() | setId(String id) |
| `Images` | [`List<ImageObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/structures/image-object.md) | Required | The cover art for the album in various sizes, widest first. | List<ImageObject> getImages() | setImages(List<ImageObject> images) |
| `Name` | `String` | Required | The name of the album. In case of an album takedown, the value may be an empty string. | String getName() | setName(String name) |
| `ReleaseDate` | `String` | Required | The date the album was first released. | String getReleaseDate() | setReleaseDate(String releaseDate) |
| `ReleaseDatePrecision` | [`ReleaseDatePrecision`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. | ReleaseDatePrecision getReleaseDatePrecision() | setReleaseDatePrecision(ReleaseDatePrecision releaseDatePrecision) |
| `Restrictions` | [`AlbumRestrictionObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/structures/album-restriction-object.md) | Optional | Included in the response when a content restriction is applied. | AlbumRestrictionObject getRestrictions() | setRestrictions(AlbumRestrictionObject restrictions) |
| `Type` | `String` | Required, Constant | The object type.<br><br>**Value**: `"album"` | String getType() | setType(String type) |
| `Uri` | `String` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the album. | String getUri() | setUri(String uri) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.AlbumBase;
import com.spotify.api.models.AlbumRestrictionObject;
import com.spotify.api.models.AlbumType;
import com.spotify.api.models.ExternalUrlObject;
import com.spotify.api.models.ImageObject;
import com.spotify.api.models.Reason;
import com.spotify.api.models.ReleaseDatePrecision;
import java.io.IOException;
import java.util.Arrays;

AlbumBase albumBase = new AlbumBase.Builder(
    AlbumType.COMPILATION,
    9,
    Arrays.asList(
        "CA",
        "BR",
        "IT"
    ),
    new ExternalUrlObject.Builder()
        .spotify("spotify6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    "href0",
    "2up3OPMp9Tb4dAKM2erWXQ",
    Arrays.asList(
        new ImageObject.Builder(
            "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
            300,
            300
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    "name8",
    "1981-12",
    ReleaseDatePrecision.YEAR,
    "album",
    "spotify:album:2up3OPMp9Tb4dAKM2erWXQ"
)
.restrictions(new AlbumRestrictionObject.Builder()
        .reason(Reason.EXPLICIT)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



