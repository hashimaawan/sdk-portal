# Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlByb3RlY3Rpb24

Protection configuration for the Resource


# Class Name

`Protection`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `boolean` | Required | If true, prevents the Resource from being deleted | boolean getDelete() | setDelete(boolean delete) |


# Example

```java
import cloud.hetzner.api.models.Protection;

Protection protection = new Protection.Builder(
    false
)
.build();
```



