# Change Protection Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0MQ


# Class Name

`ChangeProtectionRequest1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `Boolean` | Optional | If true, prevents the Network from being deleted | Boolean getDelete() | setDelete(Boolean delete) |


# Example

```java
import cloud.hetzner.api.models.ChangeProtectionRequest1;

ChangeProtectionRequest1 changeProtectionRequest1 = new ChangeProtectionRequest1.Builder()
    .delete(true)
    .build();
```



