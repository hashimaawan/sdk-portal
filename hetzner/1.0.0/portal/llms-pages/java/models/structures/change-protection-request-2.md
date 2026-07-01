# Change Protection Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0Mg


# Class Name

`ChangeProtectionRequest2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `Boolean` | Optional | If true, prevents the Primary IP from being deleted | Boolean getDelete() | setDelete(Boolean delete) |


# Example

```java
import cloud.hetzner.api.models.ChangeProtectionRequest2;

ChangeProtectionRequest2 changeProtectionRequest2 = new ChangeProtectionRequest2.Builder()
    .delete(true)
    .build();
```



