# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `boolean` | Required | If true, prevents the Server from being deleted | boolean getDelete() | setDelete(boolean delete) |
| `Rebuild` | `boolean` | Required | If true, prevents the Server from being rebuilt | boolean getRebuild() | setRebuild(boolean rebuild) |


# Example

```java
import cloud.hetzner.api.models.Protection20;

Protection20 protection20 = new Protection20.Builder(
    false,
    false
)
.build();
```



