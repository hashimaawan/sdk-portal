# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Actions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Optional | - | List<Action> getActions() | setActions(List<Action> actions) |
| `Firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/firewall.md) | Optional | - | Firewall getFirewall() | setFirewall(Firewall firewall) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.AppliedTo;
import cloud.hetzner.api.models.AppliedToResource;
import cloud.hetzner.api.models.CreateFirewallResponse;
import cloud.hetzner.api.models.DirectionEnum;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Firewall;
import cloud.hetzner.api.models.LabelSelector;
import cloud.hetzner.api.models.ProtocolEnum;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.Rule;
import cloud.hetzner.api.models.Server;
import cloud.hetzner.api.models.StatusEnum;
import cloud.hetzner.api.models.Type5Enum;
import cloud.hetzner.api.models.Type6Enum;
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
            .build(),
            "2016-01-30T23:56:00+00:00",
            13,
            100D,
            Arrays.asList(
                new Resource.Builder(
                    38,
                    "firewall"
                )
                .build()
            ),
            "2016-01-30T23:55:00+00:00",
            StatusEnum.SUCCESS
        )
        .build(),
        new Action.Builder(
            "apply_firewall",
            new Error.Builder(
                "action_failed",
                "Action failed"
            )
            .build(),
            "2016-01-30T23:56:00+00:00",
            14,
            100D,
            Arrays.asList(
                new Resource.Builder(
                    42,
                    "server"
                )
                .build(),
                new Resource.Builder(
                    38,
                    "firewall"
                )
                .build()
            ),
            "2016-01-30T23:55:00+00:00",
            StatusEnum.SUCCESS
        )
        .build()
    ))
    .firewall(new Firewall.Builder(
        Arrays.asList(
            new AppliedTo.Builder(
                Type6Enum.SERVER
            )
            .appliedToResources(Arrays.asList(
                    new AppliedToResource.Builder()
                        .server(new Server.Builder(
                            14
                        )
                        .build())
                        .type(Type5Enum.SERVER)
                        .build()
                ))
            .labelSelector(new LabelSelector.Builder(
                    "selector8"
                )
                .build())
            .server(new Server.Builder(
                    14
                )
                .build())
            .build(),
            new AppliedTo.Builder(
                Type6Enum.SERVER
            )
            .appliedToResources(Arrays.asList(
                    new AppliedToResource.Builder()
                        .server(new Server.Builder(
                            14
                        )
                        .build())
                        .type(Type5Enum.SERVER)
                        .build()
                ))
            .labelSelector(new LabelSelector.Builder(
                    "selector8"
                )
                .build())
            .server(new Server.Builder(
                    14
                )
                .build())
            .build()
        ),
        "created6",
        4,
        "name6",
        Arrays.asList(
            new Rule.Builder(
                DirectionEnum.IN,
                ProtocolEnum.UDP
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
            .build()
        )
    )
    .labels(new LinkedHashMap<String, String>() {{
            put("key0", "labels2");
            put("key1", "labels1");
        }})
    .build())
    .build();
```



