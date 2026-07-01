# Gifs Random Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/java/x-redirect/JTI0bSUyRkdpZnMlMjUyMFJhbmRvbSUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`GifsRandomResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`Gif`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/models/structures/gif.md) | Optional | - | Gif getData() | setData(Gif data) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.giphy.api.ApiHelper;
import com.giphy.api.DateTimeHelper;
import com.giphy.api.models.Gif;
import com.giphy.api.models.GifsRandomResponse;
import com.giphy.api.models.Meta;
import java.io.IOException;
import java.util.Arrays;

GifsRandomResponse gifsRandomResponse = new GifsRandomResponse.Builder()
    .data(new Gif.Builder()
        .bitlyUrl("bitly_url0")
        .contentUrl("content_url4")
        .createDatetime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .embdedUrl("embded_url8")
        .featuredTags(Arrays.asList(
            "featured_tags0"
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .meta(new Meta.Builder()
        .msg("msg8")
        .responseId("response_id0")
        .status(98)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



