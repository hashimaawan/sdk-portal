# Networks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`NetworksResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Network` | [`Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/network.md) | Optional | - | Network getNetwork() | setNetwork(Network network) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Network;
import cloud.hetzner.api.models.NetworksResponse1;
import cloud.hetzner.api.models.Protection11;
import cloud.hetzner.api.models.Route;
import cloud.hetzner.api.models.Subnet;
import cloud.hetzner.api.models.Type42;
import java.io.IOException;
import java.util.Arrays;

NetworksResponse1 networksResponse1 = new NetworksResponse1.Builder()
    .network(new Network.Builder(
        "created4",
        78,
        "ip_range6",
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        "name4",
        new Protection11.Builder(
            false
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        Arrays.asList(
            new Route.Builder(
                "destination8",
                "gateway6"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Route.Builder(
                "destination8",
                "gateway6"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Route.Builder(
                "destination8",
                "gateway6"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        Arrays.asList(
            93
        ),
        Arrays.asList(
            new Subnet.Builder(
                "gateway4",
                "network_zone2",
                Type42.CLOUD
            )
            .ipRange("ip_range6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
    )
    .loadBalancers(Arrays.asList(
            208
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



