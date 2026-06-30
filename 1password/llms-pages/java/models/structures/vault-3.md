# Vault 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRlZhdWx0Mw

*This model accepts additional fields of type Object.*


# Class Name

`Vault3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` | String getId() | setId(String id) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import local.m1password.ApiHelper;
import local.m1password.models.Vault3;

Vault3 vault3 = new Vault3.Builder()
    .id("id0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



