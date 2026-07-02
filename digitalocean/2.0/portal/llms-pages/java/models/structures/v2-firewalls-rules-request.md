# V2 Firewalls Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2FirewallsRulesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `InboundRules` | [`List<InboundRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/inbound-rule.md) | Required | - | List<InboundRule> getInboundRules() | setInboundRules(List<InboundRule> inboundRules) |
| `OutboundRules` | [`List<OutboundRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/outbound-rule.md) | Required | - | List<OutboundRule> getOutboundRules() | setOutboundRules(List<OutboundRule> outboundRules) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Destinations;
import com.digitalocean.api.models.InboundRule;
import com.digitalocean.api.models.OutboundRule;
import com.digitalocean.api.models.Protocol;
import com.digitalocean.api.models.Sources;
import com.digitalocean.api.models.V2FirewallsRulesRequest;
import java.io.IOException;
import java.util.Arrays;

V2FirewallsRulesRequest v2FirewallsRulesRequest = new V2FirewallsRulesRequest.Builder(
    Arrays.asList(
        new InboundRule.Builder(
            "8000",
            Protocol.TCP,
            new Sources.Builder()
                .addresses(Arrays.asList(
                    "1.2.3.4",
                    "18.0.0.0/8"
                ))
                .dropletIds(Arrays.asList(
                    8043964
                ))
                .kubernetesIds(Arrays.asList(
                    "41b74c5d-9bd0-5555-5555-a57c495b81a3"
                ))
                .loadBalancerUids(Arrays.asList(
                    "4de7ac8b-495b-4884-9a69-1050c6793cd6"
                ))
                .tags(Arrays.asList(
                    "tags1",
                    "tags2",
                    "tags3"
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    Arrays.asList(
        new OutboundRule.Builder(
            "8000",
            Protocol.TCP,
            new Destinations.Builder()
                .addresses(Arrays.asList(
                    "1.2.3.4",
                    "18.0.0.0/8"
                ))
                .dropletIds(Arrays.asList(
                    8043964
                ))
                .kubernetesIds(Arrays.asList(
                    "41b74c5d-9bd0-5555-5555-a57c495b81a3"
                ))
                .loadBalancerUids(Arrays.asList(
                    "4de7ac8b-495b-4884-9a69-1050c6793cd6"
                ))
                .tags(Arrays.asList(
                    "tags7",
                    "tags8",
                    "tags9"
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



