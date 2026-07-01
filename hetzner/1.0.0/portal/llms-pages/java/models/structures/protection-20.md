# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server

*This model accepts additional fields of type Object.*


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `boolean` | Required | If true, prevents the Server from being deleted | boolean getDelete() | setDelete(boolean delete) |
| `Rebuild` | `boolean` | Required | If true, prevents the Server from being rebuilt | boolean getRebuild() | setRebuild(boolean rebuild) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Protection20;
import java.io.IOException;

Protection20 protection20 = new Protection20.Builder(
    false,
    false
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



