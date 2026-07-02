# Taint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlRhaW50

*This model accepts additional fields of type Object.*


# Class Name

`Taint`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Effect` | [`Effect`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/effect.md) | Optional | How the node reacts to pods that it won't tolerate. Available effect values are `NoSchedule`, `PreferNoSchedule`, and `NoExecute`. | Effect getEffect() | setEffect(Effect effect) |
| `Key` | `String` | Optional | An arbitrary string. The `key` and `value` fields of the `taint` object form a key-value pair. For example, if the value of the `key` field is "special" and the value of the `value` field is "gpu", the key value pair would be `special=gpu`. | String getKey() | setKey(String key) |
| `Value` | `String` | Optional | An arbitrary string. The `key` and `value` fields of the `taint` object form a key-value pair. For example, if the value of the `key` field is "special" and the value of the `value` field is "gpu", the key value pair would be `special=gpu`. | String getValue() | setValue(String value) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Effect;
import com.digitalocean.api.models.Taint;
import java.io.IOException;

Taint taint = new Taint.Builder()
    .effect(Effect.NOSCHEDULE)
    .key("priority")
    .value("high")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



