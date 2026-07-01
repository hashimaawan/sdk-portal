# Gifs Search Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/java/x-redirect/JTI0bSUyRkdpZnMlMjUyMFNlYXJjaCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`GifsSearchResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<Gif>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/models/structures/gif.md) | Optional | - | List<Gif> getData() | setData(List<Gif> data) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. | Meta getMeta() | setMeta(Meta meta) |
| `Pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/models/structures/pagination.md) | Optional | The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions. | Pagination getPagination() | setPagination(Pagination pagination) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.giphy.api.ApiHelper;
import com.giphy.api.DateTimeHelper;
import com.giphy.api.models.Gif;
import com.giphy.api.models.GifsSearchResponse;
import com.giphy.api.models.Meta;
import com.giphy.api.models.Pagination;
import java.io.IOException;
import java.util.Arrays;

GifsSearchResponse gifsSearchResponse = new GifsSearchResponse.Builder()
    .data(Arrays.asList(
        new Gif.Builder()
            .bitlyUrl("bitly_url0")
            .contentUrl("content_url4")
            .createDatetime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .embdedUrl("embded_url8")
            .featuredTags(Arrays.asList(
                "featured_tags0"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Gif.Builder()
            .bitlyUrl("bitly_url0")
            .contentUrl("content_url4")
            .createDatetime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .embdedUrl("embded_url8")
            .featuredTags(Arrays.asList(
                "featured_tags0"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Gif.Builder()
            .bitlyUrl("bitly_url0")
            .contentUrl("content_url4")
            .createDatetime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .embdedUrl("embded_url8")
            .featuredTags(Arrays.asList(
                "featured_tags0"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .meta(new Meta.Builder()
        .msg("msg8")
        .responseId("response_id0")
        .status(98)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .pagination(new Pagination.Builder()
        .count(192)
        .offset(240)
        .totalCount(100)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



