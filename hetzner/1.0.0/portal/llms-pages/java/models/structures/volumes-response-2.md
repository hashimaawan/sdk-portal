# Volumes Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type Object.*


# Class Name

`VolumesResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/volume-1.md) | Required | - | Volume1 getVolume() | setVolume(Volume1 volume) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Location16;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Status113;
import cloud.hetzner.api.models.Volume1;
import cloud.hetzner.api.models.VolumesResponse2;
import java.io.IOException;
import java.util.LinkedHashMap;

VolumesResponse2 volumesResponse2 = new VolumesResponse2.Builder(
    new Volume1.Builder(
        "2016-01-30T23:55:00+00:00",
        "xfs",
        42,
        new LinkedHashMap<String, String>() {{
            put("key0", "labels8");
            put("key1", "labels9");
            put("key2", "labels0");
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
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "my-resource",
        new Protection.Builder(
            false
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        12,
        42D,
        Status113.AVAILABLE
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



