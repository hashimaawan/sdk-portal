# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Image` | `String` | Required | ID or name of Image to rebuilt from. | String getImage() | setImage(String image) |


# Example

```java
import cloud.hetzner.api.models.RebuildServerRequest;

RebuildServerRequest rebuildServerRequest = new RebuildServerRequest.Builder(
    "ubuntu-20.04"
)
.build();
```



