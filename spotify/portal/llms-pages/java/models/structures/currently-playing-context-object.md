# Currently Playing Context Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/java/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdDb250ZXh0T2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`CurrentlyPlayingContextObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Device` | [`DeviceObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/device-object.md) | Optional | The device that is currently active. | DeviceObject getDevice() | setDevice(DeviceObject device) |
| `RepeatState` | `String` | Optional | off, track, context | String getRepeatState() | setRepeatState(String repeatState) |
| `ShuffleState` | `Boolean` | Optional | If shuffle is on or off. | Boolean getShuffleState() | setShuffleState(Boolean shuffleState) |
| `Context` | [`ContextObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. | ContextObject getContext() | setContext(ContextObject context) |
| `Timestamp` | `Long` | Optional | Unix Millisecond Timestamp when data was fetched. | Long getTimestamp() | setTimestamp(Long timestamp) |
| `ProgressMs` | `Integer` | Optional | Progress into the currently playing track or episode. Can be `null`. | Integer getProgressMs() | setProgressMs(Integer progressMs) |
| `IsPlaying` | `Boolean` | Optional | If something is currently playing, return `true`. | Boolean getIsPlaying() | setIsPlaying(Boolean isPlaying) |
| `Item` | [`CurrentlyPlayingContextObjectItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/oneof-anyof-definitions/currently-playing-context-object-item.md) | Optional | This is a container for one-of cases. | CurrentlyPlayingContextObjectItem getItem() | setItem(CurrentlyPlayingContextObjectItem item) |
| `CurrentlyPlayingType` | `String` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. | String getCurrentlyPlayingType() | setCurrentlyPlayingType(String currentlyPlayingType) |
| `Actions` | [`DisallowsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. | DisallowsObject getActions() | setActions(DisallowsObject actions) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.ContextObject;
import com.spotify.api.models.CurrentlyPlayingContextObject;
import com.spotify.api.models.DeviceObject;
import com.spotify.api.models.ExternalUrlObject;
import java.io.IOException;

CurrentlyPlayingContextObject currentlyPlayingContextObject = new CurrentlyPlayingContextObject.Builder()
    .device(new DeviceObject.Builder()
        .id("id6")
        .isActive(false)
        .isPrivateSession(false)
        .isRestricted(false)
        .name("name6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .repeatState("repeat_state8")
    .shuffleState(false)
    .context(new ContextObject.Builder()
        .type("type8")
        .href("href4")
        .externalUrls(new ExternalUrlObject.Builder()
            .spotify("spotify6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .uri("uri6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .timestamp(48L)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



