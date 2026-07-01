# Update Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZVZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`UpdateVolumeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Labels` | [`Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) | Labels2 getLabels() | setLabels(Labels2 labels) |
| `Name` | `String` | Required | New Volume name | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Labels2;
import cloud.hetzner.api.models.UpdateVolumeRequest;
import java.io.IOException;

UpdateVolumeRequest updateVolumeRequest = new UpdateVolumeRequest.Builder(
    "database-storage"
)
.labels(new Labels2.Builder()
        .labelkey("labelkey4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



