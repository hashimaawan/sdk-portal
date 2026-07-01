# Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkZpcmV3YWxsUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`FirewallResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/firewall.md) | Required | - | Firewall getFirewall() | setFirewall(Firewall firewall) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.AppliedTo;
import cloud.hetzner.api.models.AppliedToResource;
import cloud.hetzner.api.models.Direction;
import cloud.hetzner.api.models.Firewall;
import cloud.hetzner.api.models.FirewallResponse;
import cloud.hetzner.api.models.LabelSelector;
import cloud.hetzner.api.models.Protocol;
import cloud.hetzner.api.models.Rule;
import cloud.hetzner.api.models.Server;
import cloud.hetzner.api.models.Type5;
import cloud.hetzner.api.models.Type6;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

FirewallResponse firewallResponse = new FirewallResponse.Builder(
    new Firewall.Builder(
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
            .build()
        ),
        "2016-01-30T23:55:00+00:00",
        42,
        "my-resource",
        Arrays.asList(
            new Rule.Builder(
                Direction.IN,
                Protocol.UDP
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
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
    )
    .labels(new LinkedHashMap<String, String>() {{
            put("key0", "labels2");
            put("key1", "labels1");
        }})
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



