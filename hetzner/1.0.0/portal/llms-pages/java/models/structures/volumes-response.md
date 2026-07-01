# Volumes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNl


# Class Name

`VolumesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |
| `Volumes` | [`List<Volume1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/volume-1.md) | Required | - | List<Volume1> getVolumes() | setVolumes(List<Volume1> volumes) |


# Example

```java
import cloud.hetzner.api.models.Location16;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Status113Enum;
import cloud.hetzner.api.models.Volume1;
import cloud.hetzner.api.models.VolumesResponse;
import java.util.Arrays;
import java.util.LinkedHashMap;

VolumesResponse volumesResponse = new VolumesResponse.Builder(
    Arrays.asList(
        new Volume1.Builder(
            "2016-01-30T23:55:00+00:00",
            "xfs",
            42,
            new LinkedHashMap<String, String>() {{
                put("key0", "labels4");
            }},
            "/dev/disk/by-id/scsi-0HC_Volume_4711",
            new Location16.Builder(
                "Falkenstein",
                "DE",
                "Falkenstein DC Park 1",
                1D,
                50.47612D,
                12.370071D,
                "fsn1",
                "eu-central"
            )
            .build(),
            "my-resource",
            new Protection.Builder(
                false
            )
            .build(),
            12,
            42D,
            Status113Enum.AVAILABLE
        )
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



