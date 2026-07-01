# Protection 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByb3RlY3Rpb24xMQ

Protection configuration for the Network

*This model accepts additional fields of type Object.*


# Class Name

`Protection11`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `boolean` | Required | If true, prevents the Network from being deleted | boolean getDelete() | setDelete(boolean delete) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Protection11;
import java.io.IOException;

Protection11 protection11 = new Protection11.Builder(
    false
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



