# Alert

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkFsZXJ0

*This model accepts additional fields of type Object.*


# Class Name

`Alert`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Disabled` | `Boolean` | Optional | Is the alert disabled? | Boolean getDisabled() | setDisabled(Boolean disabled) |
| `Operator` | [`Operator`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/operator.md) | Optional | **Default**: `Operator.UNSPECIFIED_OPERATOR` | Operator getOperator() | setOperator(Operator operator) |
| `Rule` | [`Rule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/rule.md) | Optional | **Default**: `Rule.UNSPECIFIED_RULE` | Rule getRule() | setRule(Rule rule) |
| `Value` | `Double` | Optional | Threshold value for alert | Double getValue() | setValue(Double value) |
| `Window` | [`Window`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/window.md) | Optional | **Default**: `Window.UNSPECIFIED_WINDOW` | Window getWindow() | setWindow(Window window) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Alert;
import com.digitalocean.api.models.Operator;
import com.digitalocean.api.models.Rule;
import com.digitalocean.api.models.Window;
import java.io.IOException;

Alert alert = new Alert.Builder()
    .disabled(false)
    .operator(Operator.GREATER_THAN)
    .rule(Rule.CPU_UTILIZATION)
    .value(2.32D)
    .window(Window.FIVE_MINUTES)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



