# V2 Firewalls Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`V2FirewallsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/firewall.md) | Optional | - | Firewall getFirewall() | setFirewall(Firewall firewall) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Firewall;
import com.digitalocean.api.models.PendingChange;
import com.digitalocean.api.models.V2FirewallsResponse1;
import java.io.IOException;
import java.util.Arrays;

V2FirewallsResponse1 v2FirewallsResponse1 = new V2FirewallsResponse1.Builder()
    .firewall(new Firewall.Builder()
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .dropletIds(Arrays.asList(
            67
        ))
        .id("id6")
        .name("name6")
        .pendingChanges(Arrays.asList(
            null,
            new PendingChange.Builder()
                .build(),
            new PendingChange.Builder()
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



