# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkZpcmV3YWxs


# Class Name

`Firewall`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AppliedTo` | [`List<AppliedTo>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/applied-to.md) | Required | - | List<AppliedTo> getAppliedTo() | setAppliedTo(List<AppliedTo> appliedTo) |
| `Created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) | String getCreated() | setCreated(String created) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Labels` | `Map<String, String>` | Optional | User-defined labels (key-value pairs) | Map<String, String> getLabels() | setLabels(Map<String, String> labels) |
| `Name` | `String` | Required | Name of the Resource. Must be unique per Project. | String getName() | setName(String name) |
| `Rules` | [`List<Rule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/rule.md) | Required | - | List<Rule> getRules() | setRules(List<Rule> rules) |


# Example

```java
import cloud.hetzner.api.models.AppliedTo;
import cloud.hetzner.api.models.AppliedToResource;
import cloud.hetzner.api.models.DirectionEnum;
import cloud.hetzner.api.models.Firewall;
import cloud.hetzner.api.models.LabelSelector;
import cloud.hetzner.api.models.ProtocolEnum;
import cloud.hetzner.api.models.Rule;
import cloud.hetzner.api.models.Server;
import cloud.hetzner.api.models.Type5Enum;
import cloud.hetzner.api.models.Type6Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

Firewall firewall = new Firewall.Builder(
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
        put("key0", "labels2");
        put("key1", "labels1");
    }})
.build();
```



