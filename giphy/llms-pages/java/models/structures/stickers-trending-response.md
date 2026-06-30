# Stickers Trending Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/java/x-redirect/JTI0bSUyRlN0aWNrZXJzJTI1MjBUcmVuZGluZyUyNTIwUmVzcG9uc2U


# Class Name

`StickersTrendingResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<Gif>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/gif.md) | Optional | - | List<Gif> getData() | setData(List<Gif> data) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. | Meta getMeta() | setMeta(Meta meta) |
| `Pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/pagination.md) | Optional | The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions. | Pagination getPagination() | setPagination(Pagination pagination) |


# Example

```java
import com.giphy.api.DateTimeHelper;
import com.giphy.api.models.Gif;
import com.giphy.api.models.Meta;
import com.giphy.api.models.Pagination;
import com.giphy.api.models.StickersTrendingResponse;
import java.util.Arrays;

StickersTrendingResponse stickersTrendingResponse = new StickersTrendingResponse.Builder()
    .data(Arrays.asList(
        new Gif.Builder()
            .bitlyUrl("bitly_url0")
            .contentUrl("content_url4")
            .createDatetime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .embdedUrl("embded_url8")
            .featuredTags(Arrays.asList(
                "featured_tags0"
            ))
            .build()
    ))
    .meta(new Meta.Builder()
        .msg("msg8")
        .responseId("response_id0")
        .status(98)
        .build())
    .pagination(new Pagination.Builder()
        .count(192)
        .offset(240)
        .totalCount(100)
        .build())
    .build();
```



