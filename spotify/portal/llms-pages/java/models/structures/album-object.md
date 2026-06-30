# Album Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/java/x-redirect/JTI0bSUyRkFsYnVtT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`AlbumObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AlbumType` | [`AlbumType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/enumerations/album-type.md) | Required | The type of the album. | AlbumType getAlbumType() | setAlbumType(AlbumType albumType) |
| `TotalTracks` | `int` | Required | The number of tracks in the album. | int getTotalTracks() | setTotalTracks(int totalTracks) |
| `AvailableMarkets` | `List<String>` | Required | The markets in which the album is available: [ISO 3166-1 alpha-2 country codes](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). _**NOTE**: an album is considered available in a market when at least 1 of its tracks is available in that market._ | List<String> getAvailableMarkets() | setAvailableMarkets(List<String> availableMarkets) |
| `ExternalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/external-url-object.md) | Required | Known external URLs for this album. | ExternalUrlObject getExternalUrls() | setExternalUrls(ExternalUrlObject externalUrls) |
| `Href` | `String` | Required | A link to the Web API endpoint providing full details of the album. | String getHref() | setHref(String href) |
| `Id` | `String` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the album. | String getId() | setId(String id) |
| `Images` | [`List<ImageObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/image-object.md) | Required | The cover art for the album in various sizes, widest first. | List<ImageObject> getImages() | setImages(List<ImageObject> images) |
| `Name` | `String` | Required | The name of the album. In case of an album takedown, the value may be an empty string. | String getName() | setName(String name) |
| `ReleaseDate` | `String` | Required | The date the album was first released. | String getReleaseDate() | setReleaseDate(String releaseDate) |
| `ReleaseDatePrecision` | [`ReleaseDatePrecision`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. | ReleaseDatePrecision getReleaseDatePrecision() | setReleaseDatePrecision(ReleaseDatePrecision releaseDatePrecision) |
| `Restrictions` | [`AlbumRestrictionObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/album-restriction-object.md) | Optional | Included in the response when a content restriction is applied. | AlbumRestrictionObject getRestrictions() | setRestrictions(AlbumRestrictionObject restrictions) |
| `Type` | `String` | Required, Constant | The object type.<br><br>**Value**: `"album"` | String getType() | setType(String type) |
| `Uri` | `String` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the album. | String getUri() | setUri(String uri) |
| `Artists` | [`List<SimplifiedArtistObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/simplified-artist-object.md) | Required | The artists of the album. Each artist object includes a link in `href` to more detailed information about the artist. | List<SimplifiedArtistObject> getArtists() | setArtists(List<SimplifiedArtistObject> artists) |
| `Tracks` | [`PagingSimplifiedTrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/paging-simplified-track-object.md) | Required | The tracks of the album. | PagingSimplifiedTrackObject getTracks() | setTracks(PagingSimplifiedTrackObject tracks) |
| `Copyrights` | [`List<CopyrightObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/copyright-object.md) | Required | The copyright statements of the album. | List<CopyrightObject> getCopyrights() | setCopyrights(List<CopyrightObject> copyrights) |
| `ExternalIds` | [`ExternalIdObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/external-id-object.md) | Required | Known external IDs for the album. | ExternalIdObject getExternalIds() | setExternalIds(ExternalIdObject externalIds) |
| `Genres` | `List<String>` | Required | A list of the genres the album is associated with. If not yet classified, the array is empty. | List<String> getGenres() | setGenres(List<String> genres) |
| `Label` | `String` | Required | The label associated with the album. | String getLabel() | setLabel(String label) |
| `Popularity` | `int` | Required | The popularity of the album. The value will be between 0 and 100, with 100 being the most popular. | int getPopularity() | setPopularity(int popularity) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.AlbumObject;
import com.spotify.api.models.AlbumRestrictionObject;
import com.spotify.api.models.AlbumType;
import com.spotify.api.models.CopyrightObject;
import com.spotify.api.models.ExternalIdObject;
import com.spotify.api.models.ExternalUrlObject;
import com.spotify.api.models.ImageObject;
import com.spotify.api.models.PagingSimplifiedTrackObject;
import com.spotify.api.models.Reason;
import com.spotify.api.models.ReleaseDatePrecision;
import com.spotify.api.models.SimplifiedArtistObject;
import com.spotify.api.models.SimplifiedTrackObject;
import com.spotify.api.models.Type;
import java.io.IOException;
import java.util.Arrays;

AlbumObject albumObject = new AlbumObject.Builder(
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
    "href8",
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
    "name6",
    "1981-12",
    ReleaseDatePrecision.YEAR,
    "album",
    "spotify:album:2up3OPMp9Tb4dAKM2erWXQ",
    Arrays.asList(
        new SimplifiedArtistObject.Builder()
            .externalUrls(new ExternalUrlObject.Builder()
                .spotify("spotify6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .href("href2")
            .id("id0")
            .name("name0")
            .type(Type.ARTIST)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ),
    new PagingSimplifiedTrackObject.Builder(
        "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
        20,
        "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
        0,
        "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
        4,
        Arrays.asList(
            new SimplifiedTrackObject.Builder()
                .artists(Arrays.asList(
                    new SimplifiedArtistObject.Builder()
                        .externalUrls(new ExternalUrlObject.Builder()
                            .spotify("spotify6")
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                            .build())
                        .href("href2")
                        .id("id0")
                        .name("name0")
                        .type(Type.ARTIST)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
                .availableMarkets(Arrays.asList(
                    "available_markets2"
                ))
                .discNumber(244)
                .durationMs(52)
                .explicit(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        )
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    Arrays.asList(
        new CopyrightObject.Builder()
            .text("text2")
            .type("type2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ),
    new ExternalIdObject.Builder()
        .isrc("isrc8")
        .ean("ean8")
        .upc("upc2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    Arrays.asList(
        "Egg punk",
        "Noise rock"
    ),
    "label6",
    152
)
.restrictions(new AlbumRestrictionObject.Builder()
        .reason(Reason.EXPLICIT)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



