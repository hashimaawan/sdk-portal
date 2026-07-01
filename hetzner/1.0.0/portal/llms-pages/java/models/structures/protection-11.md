# Protection 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByb3RlY3Rpb24xMQ

Protection configuration for the Network


# Class Name

`Protection11`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `boolean` | Required | If true, prevents the Network from being deleted | boolean getDelete() | setDelete(boolean delete) |


# Example

```java
import cloud.hetzner.api.models.Protection11;

Protection11 protection11 = new Protection11.Builder(
    false
)
.build();
```



