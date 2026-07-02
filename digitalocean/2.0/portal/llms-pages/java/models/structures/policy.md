# Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlBvbGljeQ

*This model accepts additional fields of type Object.*


# Class Name

`Policy`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Alerts` | [`Alerts`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/alerts.md) | Required | - | Alerts getAlerts() | setAlerts(Alerts alerts) |
| `Compare` | [`Compare`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/compare.md) | Required | - | Compare getCompare() | setCompare(Compare compare) |
| `Description` | `String` | Required | - | String getDescription() | setDescription(String description) |
| `Enabled` | `boolean` | Required | - | boolean getEnabled() | setEnabled(boolean enabled) |
| `Entities` | `List<String>` | Required | - | List<String> getEntities() | setEntities(List<String> entities) |
| `Tags` | `List<String>` | Required | - | List<String> getTags() | setTags(List<String> tags) |
| `Type` | [`Type17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-17.md) | Required | - | Type17 getType() | setType(Type17 type) |
| `Uuid` | `String` | Required | - | String getUuid() | setUuid(String uuid) |
| `Value` | `double` | Required | - | double getValue() | setValue(double value) |
| `Window` | [`Window1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/window-1.md) | Required | - | Window1 getWindow() | setWindow(Window1 window) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Alerts;
import com.digitalocean.api.models.Compare;
import com.digitalocean.api.models.Policy;
import com.digitalocean.api.models.Slack;
import com.digitalocean.api.models.Type17;
import com.digitalocean.api.models.Window1;
import java.io.IOException;
import java.util.Arrays;

Policy policy = new Policy.Builder(
    new Alerts.Builder(
        Arrays.asList(
            "bob@exmaple.com"
        ),
        Arrays.asList(
            new Slack.Builder(
                "Production Alerts",
                "https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    Compare.GREATERTHAN,
    "CPU Alert",
    true,
    Arrays.asList(
        "192018292"
    ),
    Arrays.asList(
        "droplet_tag"
    ),
    Type17.ENUM_V1INSIGHTSDROPLETCPU,
    "78b3da62-27e5-49ba-ac70-5db0b5935c64",
    80D,
    Window1.ENUM_5M
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



