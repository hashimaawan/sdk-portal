# Url

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRlVybA

*This model accepts additional fields of type Object.*


# Class Name

`Url`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Href` | `String` | Required | - | String getHref() | setHref(String href) |
| `Label` | `String` | Optional | - | String getLabel() | setLabel(String label) |
| `Primary` | `Boolean` | Optional | - | Boolean getPrimary() | setPrimary(Boolean primary) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import local.m1password.ApiHelper;
import local.m1password.models.Url;

Url url = new Url.Builder(
    "href6"
)
.label("label4")
.primary(false)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



