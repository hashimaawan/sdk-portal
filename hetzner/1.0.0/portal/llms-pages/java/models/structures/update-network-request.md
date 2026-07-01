# Update Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZU5ldHdvcmtSZXF1ZXN0


# Class Name

`UpdateNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Labels` | [`Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) | Labels2 getLabels() | setLabels(Labels2 labels) |
| `Name` | `String` | Optional | New network name | String getName() | setName(String name) |


# Example

```java
import cloud.hetzner.api.models.Labels2;
import cloud.hetzner.api.models.UpdateNetworkRequest;

UpdateNetworkRequest updateNetworkRequest = new UpdateNetworkRequest.Builder()
    .labels(new Labels2.Builder()
        .labelkey("labelkey4")
        .build())
    .name("new-name")
    .build();
```



