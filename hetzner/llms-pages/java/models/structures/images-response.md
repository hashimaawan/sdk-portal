# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U


# Class Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Images` | [`List<Image>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/image.md) | Required | - | List<Image> getImages() | setImages(List<Image> images) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |


# Example

```java
import cloud.hetzner.api.models.CreatedFrom;
import cloud.hetzner.api.models.Image;
import cloud.hetzner.api.models.ImagesResponse;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.OsFlavorEnum;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Status24Enum;
import cloud.hetzner.api.models.Type22Enum;
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
            OsFlavorEnum.UBUNTU,
            "20.04",
            new Protection.Builder(
                false
            )
            .build(),
            Status24Enum.AVAILABLE,
            Type22Enum.SNAPSHOT
        )
        .rapidDeploy(false)
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
        .build()
    )
    .build())
.build();
```



