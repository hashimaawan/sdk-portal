# Section 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRlNlY3Rpb24y

*This model accepts additional fields of type Object.*


# Class Name

`Section2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Label` | `String` | Optional | - | String getLabel() | setLabel(String label) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import local.m1password.ApiHelper;
import local.m1password.models.Section2;

Section2 section2 = new Section2.Builder()
    .id("id4")
    .label("label4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



