# Label Selector 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I3

Label selector and a list of selected targets

*This model accepts additional fields of type Object.*


# Class Name

`LabelSelector7`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Selector` | `String` | Required | Label selector | String getSelector() | setSelector(String selector) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.LabelSelector7;
import java.io.IOException;

LabelSelector7 labelSelector7 = new LabelSelector7.Builder(
    "env=prod"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



