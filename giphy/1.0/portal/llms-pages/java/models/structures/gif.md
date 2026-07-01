# Gif

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/java/x-redirect/JTI0bSUyRkdpZg


# Class Name

`Gif`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BitlyUrl` | `String` | Optional | The unique bit.ly URL for this GIF | String getBitlyUrl() | setBitlyUrl(String bitlyUrl) |
| `ContentUrl` | `String` | Optional | Currently unused | String getContentUrl() | setContentUrl(String contentUrl) |
| `CreateDatetime` | `LocalDateTime` | Optional | The date this GIF was added to the GIPHY database. | LocalDateTime getCreateDatetime() | setCreateDatetime(LocalDateTime createDatetime) |
| `EmbdedUrl` | `String` | Optional | A URL used for embedding this GIF | String getEmbdedUrl() | setEmbdedUrl(String embdedUrl) |
| `FeaturedTags` | `List<String>` | Optional | An array of featured tags for this GIF (Note: Not available when using the Public Beta Key) | List<String> getFeaturedTags() | setFeaturedTags(List<String> featuredTags) |
| `Id` | `String` | Optional | This GIF's unique ID | String getId() | setId(String id) |
| `Images` | [`Images`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/models/structures/images.md) | Optional | An object containing data for various available formats and sizes of this GIF. | Images getImages() | setImages(Images images) |
| `ImportDatetime` | `LocalDateTime` | Optional | The creation or upload date from this GIF's source. | LocalDateTime getImportDatetime() | setImportDatetime(LocalDateTime importDatetime) |
| `Rating` | `String` | Optional | The MPAA-style rating for this content. Examples include Y, G, PG, PG-13 and R | String getRating() | setRating(String rating) |
| `Slug` | `String` | Optional | The unique slug used in this GIF's URL | String getSlug() | setSlug(String slug) |
| `Source` | `String` | Optional | The page on which this GIF was found | String getSource() | setSource(String source) |
| `SourcePostUrl` | `String` | Optional | The URL of the webpage on which this GIF was found. | String getSourcePostUrl() | setSourcePostUrl(String sourcePostUrl) |
| `SourceTld` | `String` | Optional | The top level domain of the source URL. | String getSourceTld() | setSourceTld(String sourceTld) |
| `Tags` | `List<String>` | Optional | An array of tags for this GIF (Note: Not available when using the Public Beta Key) | List<String> getTags() | setTags(List<String> tags) |
| `TrendingDatetime` | `LocalDateTime` | Optional | The date on which this gif was marked trending, if applicable. | LocalDateTime getTrendingDatetime() | setTrendingDatetime(LocalDateTime trendingDatetime) |
| `Type` | [`TypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/models/enumerations/type.md) | Optional | Type of the gif. By default, this is almost always gif<br><br>**Default**: `TypeEnum.GIF` | TypeEnum getType() | setType(TypeEnum type) |
| `UpdateDatetime` | `LocalDateTime` | Optional | The date on which this GIF was last updated. | LocalDateTime getUpdateDatetime() | setUpdateDatetime(LocalDateTime updateDatetime) |
| `Url` | `String` | Optional | The unique URL for this GIF | String getUrl() | setUrl(String url) |
| `User` | [`User`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/models/structures/user.md) | Optional | The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more. | User getUser() | setUser(User user) |
| `Username` | `String` | Optional | The username this GIF is attached to, if applicable | String getUsername() | setUsername(String username) |


# Example

```java
import com.giphy.api.DateTimeHelper;
import com.giphy.api.models.Gif;
import com.giphy.api.models.TypeEnum;
import java.util.Arrays;

Gif gif = new Gif.Builder()
    .bitlyUrl("http://gph.is/1gsWDcL")
    .contentUrl("content_url4")
    .createDatetime(DateTimeHelper.fromRfc8601DateTime("2013-08-01 12:41:48"))
    .embdedUrl("http://giphy.com/embed/YsTs5ltWtEhnq")
    .featuredTags(Arrays.asList(
        "featured_tags0"
    ))
    .id("YsTs5ltWtEhnq")
    .importDatetime(DateTimeHelper.fromRfc8601DateTime("2013-08-01 12:41:48"))
    .rating("g")
    .slug("confused-flying-YsTs5ltWtEhnq")
    .source("http://www.reddit.com/r/reactiongifs/comments/1xpyaa/superman_goes_to_hollywood/")
    .sourcePostUrl("http://cheezburger.com/5282328320")
    .sourceTld("cheezburger.com")
    .trendingDatetime(DateTimeHelper.fromRfc8601DateTime("2013-08-01 12:41:48"))
    .type(TypeEnum.GIF)
    .updateDatetime(DateTimeHelper.fromRfc8601DateTime("2013-08-01 12:41:48"))
    .url("http://giphy.com/gifs/confused-flying-YsTs5ltWtEhnq")
    .username("JoeCool4000")
    .build();
```



