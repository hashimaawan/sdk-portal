# Gifs Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/java/x-redirect/JTI0bSUyRkdpZnMlMjUyMFJlc3BvbnNlMQ


# Class Name

`GifsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`Gif`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/gif.md) | Optional | - | Gif getData() | setData(Gif data) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. | Meta getMeta() | setMeta(Meta meta) |


# Example

```java
import com.giphy.api.DateTimeHelper;
import com.giphy.api.models.Gif;
import com.giphy.api.models.GifsResponse1;
import com.giphy.api.models.Meta;
import java.util.Arrays;

GifsResponse1 gifsResponse1 = new GifsResponse1.Builder()
    .data(new Gif.Builder()
        .bitlyUrl("bitly_url0")
        .contentUrl("content_url4")
        .createDatetime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .embdedUrl("embded_url8")
        .featuredTags(Arrays.asList(
            "featured_tags0"
        ))
        .build())
    .meta(new Meta.Builder()
        .msg("msg8")
        .responseId("response_id0")
        .status(98)
        .build())
    .build();
```



