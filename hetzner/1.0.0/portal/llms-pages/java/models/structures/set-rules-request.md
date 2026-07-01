# Set Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNldFJ1bGVzUmVxdWVzdA


# Class Name

`SetRulesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Rules` | [`List<Rule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/rule.md) | Required | Array of rules<br><br>**Constraints**: *Maximum Items*: `50` | List<Rule> getRules() | setRules(List<Rule> rules) |


# Example

```java
import cloud.hetzner.api.models.DirectionEnum;
import cloud.hetzner.api.models.ProtocolEnum;
import cloud.hetzner.api.models.Rule;
import cloud.hetzner.api.models.SetRulesRequest;
import java.util.Arrays;

SetRulesRequest setRulesRequest = new SetRulesRequest.Builder(
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
.build();
```



