# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Actions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Optional | - | List<Action> getActions() | setActions(List<Action> actions) |
| `Firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/firewall.md) | Optional | - | Firewall getFirewall() | setFirewall(Firewall firewall) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.AppliedTo;
import cloud.hetzner.api.models.AppliedToResource;
import cloud.hetzner.api.models.CreateFirewallResponse;
import cloud.hetzner.api.models.Direction;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Firewall;
import cloud.hetzner.api.models.LabelSelector;
import cloud.hetzner.api.models.Protocol;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.Rule;
import cloud.hetzner.api.models.Server;
import cloud.hetzner.api.models.Status;
import cloud.hetzner.api.models.Type5;
import cloud.hetzner.api.models.Type6;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

CreateFirewallResponse createFirewallResponse = new CreateFirewallResponse.Builder()
    .actions(Arrays.asList(
        new Action.Builder(
            "set_firewall_rules",
            new Error.Builder(
                "action_failed",
                "Action failed"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            "2016-01-30T23:56:00+00:00",
            13,
            100D,
            Arrays.asList(
                new Resource.Builder(
                    38,
                    "firewall"
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            ),
            "2016-01-30T23:55:00+00:00",
            Status.SUCCESS
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Action.Builder(
            "apply_firewall",
            new Error.Builder(
                "action_failed",
                "Action failed"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            "2016-01-30T23:56:00+00:00",
            14,
            100D,
            Arrays.asList(
                new Resource.Builder(
                    42,
                    "server"
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
                new Resource.Builder(
                    38,
                    "firewall"
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            ),
            "2016-01-30T23:55:00+00:00",
            Status.SUCCESS
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
    .firewall(new Firewall.Builder(
        Arrays.asList(
            new AppliedTo.Builder(
                Type6.SERVER
            )
            .appliedToResources(Arrays.asList(
                    new AppliedToResource.Builder()
                        .server(new Server.Builder(
                            14
                        )
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                        .type(Type5.SERVER)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
            .labelSelector(new LabelSelector.Builder(
                    "selector8"
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .server(new Server.Builder(
                    14
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new AppliedTo.Builder(
                Type6.SERVER
            )
            .appliedToResources(Arrays.asList(
                    new AppliedToResource.Builder()
                        .server(new Server.Builder(
                            14
                        )
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                        .type(Type5.SERVER)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
            .labelSelector(new LabelSelector.Builder(
                    "selector8"
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .server(new Server.Builder(
                    14
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        "created6",
        4,
        "name6",
        Arrays.asList(
            new Rule.Builder(
                Direction.IN,
                Protocol.UDP
            )
            .description("description2")
            .destinationIps(Arrays.asList(
                    "destination_ips1",
                    "destination_ips2",
                    "destination_ips3"
                ))
            .port("port8")
            .sourceIps(Arrays.asList(
                    "source_ips1",
                    "source_ips2",
                    "source_ips3"
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
    )
    .labels(new LinkedHashMap<String, String>() {{
            put("key0", "labels2");
            put("key1", "labels1");
        }})
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



