# Images Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0


# Class Name

`ImagesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `Boolean` | Optional | If true, prevents the snapshot from being deleted | Boolean getDelete() | setDelete(Boolean delete) |


# Example

```java
import cloud.hetzner.api.models.ImagesActionsChangeProtectionRequest;

ImagesActionsChangeProtectionRequest imagesActionsChangeProtectionRequest = new ImagesActionsChangeProtectionRequest.Builder()
    .delete(true)
    .build();
```



