# Volumes Actions Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA


# Class Name

`VolumesActionsResizeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Size` | `double` | Required | New Volume size in GB (must be greater than current size) | double getSize() | setSize(double size) |


# Example

```java
import cloud.hetzner.api.models.VolumesActionsResizeRequest;

VolumesActionsResizeRequest volumesActionsResizeRequest = new VolumesActionsResizeRequest.Builder(
    50D
)
.build();
```



