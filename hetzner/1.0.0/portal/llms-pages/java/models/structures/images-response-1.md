# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/image.md) | Optional | - | Image getImage() | setImage(Image image) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreatedFrom;
import cloud.hetzner.api.models.Image;
import cloud.hetzner.api.models.ImagesResponse1;
import cloud.hetzner.api.models.OsFlavor;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Status24;
import cloud.hetzner.api.models.Type22;
import java.io.IOException;
import java.util.LinkedHashMap;

ImagesResponse1 imagesResponse1 = new ImagesResponse1.Builder()
    .image(new Image.Builder(
        186,
        "created6",
        new CreatedFrom.Builder(
            60,
            "name6"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "deleted4",
        "deprecated8",
        "description6",
        244.18D,
        128,
        141.34D,
        new LinkedHashMap<String, String>() {{
            put("key0", "labels4");
        }},
        "name6",
        OsFlavor.DEBIAN,
        "os_version4",
        new Protection.Builder(
            false
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        Status24.UNAVAILABLE,
        Type22.APP
    )
    .rapidDeploy(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



