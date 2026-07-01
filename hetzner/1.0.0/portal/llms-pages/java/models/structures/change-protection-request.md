# Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0


# Class Name

`ChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `Boolean` | Optional | If true, prevents the Floating IP from being deleted | Boolean getDelete() | setDelete(Boolean delete) |


# Example

```java
import cloud.hetzner.api.models.ChangeProtectionRequest;

ChangeProtectionRequest changeProtectionRequest = new ChangeProtectionRequest.Builder()
    .delete(true)
    .build();
```



