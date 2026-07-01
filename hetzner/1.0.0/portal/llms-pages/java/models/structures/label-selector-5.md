# Label Selector 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I1

Configuration for type label_selector, required if type is `label_selector`

*This model accepts additional fields of type Object.*


# Class Name

`LabelSelector5`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Selector` | `String` | Required | Label selector | String getSelector() | setSelector(String selector) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.LabelSelector5;
import java.io.IOException;

LabelSelector5 labelSelector5 = new LabelSelector5.Builder(
    "env=prod"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



