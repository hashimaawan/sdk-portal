# Episode Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/java/x-redirect/JTI0bSUyRkVwaXNvZGVPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`EpisodeObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AudioPreviewUrl` | `String` | Required | A URL to a 30 second preview (MP3 format) of the episode. `null` if not available. | String getAudioPreviewUrl() | setAudioPreviewUrl(String audioPreviewUrl) |
| `Description` | `String` | Required | A description of the episode. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. | String getDescription() | setDescription(String description) |
| `HtmlDescription` | `String` | Required | A description of the episode. This field may contain HTML tags. | String getHtmlDescription() | setHtmlDescription(String htmlDescription) |
| `DurationMs` | `int` | Required | The episode length in milliseconds. | int getDurationMs() | setDurationMs(int durationMs) |
| `Explicit` | `boolean` | Required | Whether or not the episode has explicit content (true = yes it does; false = no it does not OR unknown). | boolean getExplicit() | setExplicit(boolean explicit) |
| `ExternalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/external-url-object.md) | Required | External URLs for this episode. | ExternalUrlObject getExternalUrls() | setExternalUrls(ExternalUrlObject externalUrls) |
| `Href` | `String` | Required | A link to the Web API endpoint providing full details of the episode. | String getHref() | setHref(String href) |
| `Id` | `String` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the episode. | String getId() | setId(String id) |
| `Images` | [`List<ImageObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/image-object.md) | Required | The cover art for the episode in various sizes, widest first. | List<ImageObject> getImages() | setImages(List<ImageObject> images) |
| `IsExternallyHosted` | `boolean` | Required | True if the episode is hosted outside of Spotify's CDN. | boolean getIsExternallyHosted() | setIsExternallyHosted(boolean isExternallyHosted) |
| `IsPlayable` | `boolean` | Required | True if the episode is playable in the given market. Otherwise false. | boolean getIsPlayable() | setIsPlayable(boolean isPlayable) |
| `Language` | `String` | Optional | The language used in the episode, identified by a [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. This field is deprecated and might be removed in the future. Please use the `languages` field instead. | String getLanguage() | setLanguage(String language) |
| `Languages` | `List<String>` | Required | A list of the languages used in the episode, identified by their [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639) code. | List<String> getLanguages() | setLanguages(List<String> languages) |
| `Name` | `String` | Required | The name of the episode. | String getName() | setName(String name) |
| `ReleaseDate` | `String` | Required | The date the episode was first released, for example `"1981-12-15"`. Depending on the precision, it might be shown as `"1981"` or `"1981-12"`. | String getReleaseDate() | setReleaseDate(String releaseDate) |
| `ReleaseDatePrecision` | [`ReleaseDatePrecision`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. | ReleaseDatePrecision getReleaseDatePrecision() | setReleaseDatePrecision(ReleaseDatePrecision releaseDatePrecision) |
| `ResumePoint` | [`ResumePointObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/resume-point-object.md) | Optional | The user's most recent position in the episode. Set if the supplied access token is a user token and has the scope 'user-read-playback-position'. | ResumePointObject getResumePoint() | setResumePoint(ResumePointObject resumePoint) |
| `Type` | `String` | Required, Constant | The object type.<br><br>**Value**: `"episode"` | String getType() | setType(String type) |
| `Uri` | `String` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the episode. | String getUri() | setUri(String uri) |
| `Restrictions` | [`EpisodeRestrictionObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/episode-restriction-object.md) | Optional | Included in the response when a content restriction is applied. | EpisodeRestrictionObject getRestrictions() | setRestrictions(EpisodeRestrictionObject restrictions) |
| `Show` | [`ShowBase`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/show-base.md) | Required | The show on which the episode belongs. | ShowBase getShow() | setShow(ShowBase show) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.CopyrightObject;
import com.spotify.api.models.EpisodeObject;
import com.spotify.api.models.EpisodeRestrictionObject;
import com.spotify.api.models.ExternalUrlObject;
import com.spotify.api.models.ImageObject;
import com.spotify.api.models.ReleaseDatePrecision;
import com.spotify.api.models.ResumePointObject;
import com.spotify.api.models.ShowBase;
import java.io.IOException;
import java.util.Arrays;

EpisodeObject episodeObject = new EpisodeObject.Builder(
    "https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17",
    "A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.\n",
    "<p>A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.</p>\n",
    1686230,
    false,
    new ExternalUrlObject.Builder()
        .spotify("spotify6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    "https://api.spotify.com/v1/episodes/5Xt5DXGzch68nYYamXrNxZ",
    "5Xt5DXGzch68nYYamXrNxZ",
    Arrays.asList(
        new ImageObject.Builder(
            "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
            300,
            300
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    false,
    false,
    Arrays.asList(
        "fr",
        "en"
    ),
    "Starting Your Own Podcast: Tips, Tricks, and Advice From Anchor Creators\n",
    "1981-12-15",
    ReleaseDatePrecision.DAY,
    "episode",
    "spotify:episode:0zLhl3WsOCQHbe1BPTiHgr",
    new ShowBase.Builder(
        Arrays.asList(
            "available_markets0",
            "available_markets1",
            "available_markets2"
        ),
        Arrays.asList(
            new CopyrightObject.Builder()
                .text("text2")
                .type("type2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ),
        "description4",
        "html_description4",
        false,
        new ExternalUrlObject.Builder()
            .spotify("spotify6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        "href8",
        "id6",
        Arrays.asList(
            new ImageObject.Builder(
                "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
                300,
                300
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        false,
        Arrays.asList(
            "languages7",
            "languages6",
            "languages5"
        ),
        "media_type6",
        "name6",
        "publisher6",
        "show",
        "uri0",
        198
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.language("en")
.resumePoint(new ResumePointObject.Builder()
        .fullyPlayed(false)
        .resumePositionMs(254)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.restrictions(new EpisodeRestrictionObject.Builder()
        .reason("reason0")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



