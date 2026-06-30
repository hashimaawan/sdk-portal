# Firewalls Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkZpcmV3YWxsc1Jlc3BvbnNl


# Class Name

`FirewallsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Firewalls` | [`List<Firewall>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/firewall.md) | Required | - | List<Firewall> getFirewalls() | setFirewalls(List<Firewall> firewalls) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |


# Example

```java
import cloud.hetzner.api.models.AppliedTo;
import cloud.hetzner.api.models.AppliedToResource;
import cloud.hetzner.api.models.DirectionEnum;
import cloud.hetzner.api.models.Firewall;
import cloud.hetzner.api.models.FirewallsResponse;
import cloud.hetzner.api.models.LabelSelector;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.ProtocolEnum;
import cloud.hetzner.api.models.Rule;
import cloud.hetzner.api.models.Server;
import cloud.hetzner.api.models.Type5Enum;
import cloud.hetzner.api.models.Type6Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

FirewallsResponse firewallsResponse = new FirewallsResponse.Builder(
    Arrays.asList(
        new Firewall.Builder(
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
                .build()
            ),
            "2016-01-30T23:55:00+00:00",
            42,
            "my-resource",
            Arrays.asList(
                new Rule.Builder(
                    DirectionEnum.IN,
                    ProtocolEnum.UDP
                )
                .description("description2")
                .destinationIps(Arrays.asList(
                        "28.239.13.1/32",
                        "28.239.14.0/24",
                        "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128"
                    ))
                .port("80")
                .sourceIps(Arrays.asList(
                        "28.239.13.1/32",
                        "28.239.14.0/24",
                        "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128"
                    ))
                .build()
            )
        )
        .labels(new LinkedHashMap<String, String>() {{
                put("key0", "labels4");
                put("key1", "labels5");
            }})
        .build()
    )
)
.meta(new Meta.Builder(
        new Pagination.Builder(
            77.7D,
            209.18D,
            17.58D,
            13.34D,
            50.02D,
            206.64D
        )
        .build()
    )
    .build())
.build();
```



