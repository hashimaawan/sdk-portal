# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/image.md) | Optional | - | Image getImage() | setImage(Image image) |


# Example

```java
import cloud.hetzner.api.models.CreatedFrom;
import cloud.hetzner.api.models.Image;
import cloud.hetzner.api.models.ImagesResponse1;
import cloud.hetzner.api.models.OsFlavorEnum;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Status24Enum;
import cloud.hetzner.api.models.Type22Enum;
import java.util.LinkedHashMap;

ImagesResponse1 imagesResponse1 = new ImagesResponse1.Builder()
    .image(new Image.Builder(
        186,
        "created6",
        new CreatedFrom.Builder(
            60,
            "name6"
        )
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
        OsFlavorEnum.DEBIAN,
        "os_version4",
        new Protection.Builder(
            false
        )
        .build(),
        Status24Enum.UNAVAILABLE,
        Type22Enum.APP
    )
    .rapidDeploy(false)
    .build())
    .build();
```



