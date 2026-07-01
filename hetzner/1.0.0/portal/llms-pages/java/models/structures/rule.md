# Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlJ1bGU


# Class Name

`Rule`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | Description of the Rule<br><br>**Constraints**: *Maximum Length*: `255` | String getDescription() | setDescription(String description) |
| `DestinationIps` | `List<String>` | Optional | List of permitted IPv4/IPv6 addresses in CIDR notation. Use `0.0.0.0/0` to allow all IPv4 addresses and `::/0` to allow all IPv6 addresses. You can specify 100 CIDRs at most. | List<String> getDestinationIps() | setDestinationIps(List<String> destinationIps) |
| `Direction` | [`DirectionEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/direction.md) | Required | Select traffic direction on which rule should be applied. Use `source_ips` for direction `in` and `destination_ips` for direction `out`. | DirectionEnum getDirection() | setDirection(DirectionEnum direction) |
| `Port` | `String` | Optional | Port or port range to which traffic will be allowed, only applicable for protocols TCP and UDP. A port range can be specified by separating two ports with a dash, e.g `1024-5000`. | String getPort() | setPort(String port) |
| `Protocol` | [`ProtocolEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/protocol.md) | Required | Type of traffic to allow | ProtocolEnum getProtocol() | setProtocol(ProtocolEnum protocol) |
| `SourceIps` | `List<String>` | Optional | List of permitted IPv4/IPv6 addresses in CIDR notation. Use `0.0.0.0/0` to allow all IPv4 addresses and `::/0` to allow all IPv6 addresses. You can specify 100 CIDRs at most. | List<String> getSourceIps() | setSourceIps(List<String> sourceIps) |


# Example

```java
import cloud.hetzner.api.models.DirectionEnum;
import cloud.hetzner.api.models.ProtocolEnum;
import cloud.hetzner.api.models.Rule;
import java.util.Arrays;

Rule rule = new Rule.Builder(
    DirectionEnum.IN,
    ProtocolEnum.ESP
)
.description("description0")
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
.build();
```



