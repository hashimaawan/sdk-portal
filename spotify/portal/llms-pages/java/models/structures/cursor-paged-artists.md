# Cursor Paged Artists

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/java/x-redirect/JTI0bSUyRkN1cnNvclBhZ2VkQXJ0aXN0cw

*This model accepts additional fields of type Object.*


# Class Name

`CursorPagedArtists`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Artists` | [`CursorPagingSimplifiedArtistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/cursor-paging-simplified-artist-object.md) | Required | - | CursorPagingSimplifiedArtistObject getArtists() | setArtists(CursorPagingSimplifiedArtistObject artists) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.CursorObject;
import com.spotify.api.models.CursorPagedArtists;
import com.spotify.api.models.CursorPagingSimplifiedArtistObject;
import java.io.IOException;

CursorPagedArtists cursorPagedArtists = new CursorPagedArtists.Builder(
    new CursorPagingSimplifiedArtistObject.Builder()
        .href("href2")
        .limit(214)
        .next("next2")
        .cursors(new CursorObject.Builder()
            .after("after8")
            .before("before6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .total(52)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



