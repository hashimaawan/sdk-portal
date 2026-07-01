# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ApplyTo` | [`List<ApplyTo>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation | List<ApplyTo> getApplyTo() | setApplyTo(List<ApplyTo> applyTo) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Required | Name of the Firewall | String getName() | setName(String name) |
| `Rules` | [`List<Rule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/rule.md) | Optional | Array of rules | List<Rule> getRules() | setRules(List<Rule> rules) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ApplyTo;
import cloud.hetzner.api.models.CreateFirewallRequest;
import cloud.hetzner.api.models.Direction;
import cloud.hetzner.api.models.LabelSelector1;
import cloud.hetzner.api.models.Protocol;
import cloud.hetzner.api.models.Rule;
import cloud.hetzner.api.models.Server2;
import cloud.hetzner.api.models.Type7;
import java.io.IOException;
import java.util.Arrays;

CreateFirewallRequest createFirewallRequest = new CreateFirewallRequest.Builder(
    "Corporate Intranet Protection"
)
.applyTo(Arrays.asList(
        new ApplyTo.Builder(
            Type7.SERVER
        )
        .labelSelector(new LabelSelector1.Builder(
                "selector8"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .server(new Server2.Builder(
                14
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new ApplyTo.Builder(
            Type7.SERVER
        )
        .labelSelector(new LabelSelector1.Builder(
                "selector8"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .server(new Server2.Builder(
                14
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new ApplyTo.Builder(
            Type7.SERVER
        )
        .labelSelector(new LabelSelector1.Builder(
                "selector8"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .server(new Server2.Builder(
                14
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.labels(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.rules(Arrays.asList(
        new Rule.Builder(
            Direction.IN,
            Protocol.TCP
        )
        .description("description2")
        .destinationIps(Arrays.asList(
                "destination_ips1",
                "destination_ips2",
                "destination_ips3"
            ))
        .port("80")
        .sourceIps(Arrays.asList(
                "28.239.13.1/32",
                "28.239.14.0/24",
                "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



