# Patch

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRlBhdGNo

*This model accepts additional fields of type Object.*


# Class Name

`Patch`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Op` | [`Op`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/enumerations/op.md) | Required | - | Op getOp() | setOp(Op op) |
| `Path` | `String` | Required | An RFC6901 JSON Pointer pointing to the Item document, an Item Attribute, and Item Field by Field ID, or an Item Field Attribute | String getPath() | setPath(String path) |
| `Value` | `Object` | Optional | - | Object getValue() | setValue(Object value) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import local.m1password.ApiHelper;
import local.m1password.models.Op;
import local.m1password.models.Patch;

Patch patch = new Patch.Builder(
    Op.REMOVE,
    "/fields/06gnn2b95example10q91512p5/label"
)
.value(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



