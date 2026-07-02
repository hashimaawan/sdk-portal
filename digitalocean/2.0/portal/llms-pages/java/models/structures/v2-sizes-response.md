# V2 Sizes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBTaXplcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2SizesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Sizes` | [`List<Size>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/size.md) | Required | - | List<Size> getSizes() | setSizes(List<Size> sizes) |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links.md) | Optional | - | Links getLinks() | setLinks(Links links) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/meta.md) | Required | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.Meta;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.Size;
import com.digitalocean.api.models.V2SizesResponse;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;
import java.util.Arrays;

V2SizesResponse v2SizesResponse = new V2SizesResponse.Builder(
    Arrays.asList(
        new Size.Builder(
            true,
            "Basic",
            25,
            1024,
            0.00743999984115362D,
            5D,
            Arrays.asList(
                "ams2",
                "ams3",
                "blr1",
                "fra1",
                "lon1",
                "nyc1",
                "nyc2",
                "nyc3",
                "sfo1",
                "sfo2",
                "sfo3",
                "sgp1",
                "tor1"
            ),
            "s-1vcpu-1gb",
            1D,
            1
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    new Meta.Builder(
        64
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.links(new Links.Builder()
        .pages(LinksPages.fromPages(
            new Pages.Builder()
                .last("https://api.digitalocean.com/v2/sizes?page=64&per_page=1")
                .next("https://api.digitalocean.com/v2/sizes?page=2&per_page=1")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



