# Inbound Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkluYm91bmRSdWxl

*This model accepts additional fields of type Object.*


# Class Name

`InboundRule`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ports` | `String` | Required | The ports on which traffic will be allowed specified as a string containing a single port, a range (e.g. "8000-9000"), or "0" when all ports are open for a protocol. For ICMP rules this parameter will always return "0". | String getPorts() | setPorts(String ports) |
| `Protocol` | [`Protocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/protocol.md) | Required | The type of traffic to be allowed. This may be one of `tcp`, `udp`, or `icmp`. | Protocol getProtocol() | setProtocol(Protocol protocol) |
| `Sources` | [`Sources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/sources.md) | Required | - | Sources getSources() | setSources(Sources sources) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.InboundRule;
import com.digitalocean.api.models.Protocol;
import com.digitalocean.api.models.Sources;
import java.io.IOException;
import java.util.Arrays;

InboundRule inboundRule = new InboundRule.Builder(
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
.build();
```



