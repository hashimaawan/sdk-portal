# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Images` | [`List<Image>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/image.md) | Required | - | List<Image> getImages() | setImages(List<Image> images) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreatedFrom;
import cloud.hetzner.api.models.Image;
import cloud.hetzner.api.models.ImagesResponse;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.OsFlavor;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Status24;
import cloud.hetzner.api.models.Type22;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

ImagesResponse imagesResponse = new ImagesResponse.Builder(
    Arrays.asList(
        new Image.Builder(
            null,
            "2016-01-30T23:55:00+00:00",
            new CreatedFrom.Builder(
                1,
                "Server"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            null,
            "2018-02-28T00:00:00+00:00",
            "Ubuntu 20.04 Standard 64 bit",
            10D,
            42,
            2.3D,
            new LinkedHashMap<String, String>() {{
                put("key0", "labels0");
                put("key1", "labels1");
            }},
            "ubuntu-20.04",
            OsFlavor.UBUNTU,
            "20.04",
            new Protection.Builder(
                false
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            Status24.AVAILABLE,
            Type22.SNAPSHOT
        )
        .rapidDeploy(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.meta(new Meta.Builder(
        new Pagination.Builder(
            77.7D,
            209.18D,
            17.58D,
            13.34D,
            50.02D,
            206.64D
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



