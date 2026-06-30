# Category Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/java/x-redirect/JTI0bSUyRkNhdGVnb3J5T2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`CategoryObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Href` | `String` | Required | A link to the Web API endpoint returning full details of the category. | String getHref() | setHref(String href) |
| `Icons` | [`List<ImageObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/structures/image-object.md) | Required | The category icon, in various sizes. | List<ImageObject> getIcons() | setIcons(List<ImageObject> icons) |
| `Id` | `String` | Required | The [Spotify category ID](/documentation/web-api/concepts/spotify-uris-ids) of the category. | String getId() | setId(String id) |
| `Name` | `String` | Required | The name of the category. | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.CategoryObject;
import com.spotify.api.models.ImageObject;
import java.io.IOException;
import java.util.Arrays;

CategoryObject categoryObject = new CategoryObject.Builder(
    "href2",
    Arrays.asList(
        new ImageObject.Builder(
            "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
            300,
            300
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    "equal",
    "EQUAL"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



