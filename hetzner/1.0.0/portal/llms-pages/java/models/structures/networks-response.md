# Networks Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`NetworksResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |
| `Networks` | [`List<Network>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/network.md) | Required | - | List<Network> getNetworks() | setNetworks(List<Network> networks) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Network;
import cloud.hetzner.api.models.NetworksResponse;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.Protection11;
import cloud.hetzner.api.models.Route;
import cloud.hetzner.api.models.Subnet;
import cloud.hetzner.api.models.Type42;
import java.io.IOException;
import java.util.Arrays;

NetworksResponse networksResponse = new NetworksResponse.Builder(
    Arrays.asList(
        new Network.Builder(
            "2016-01-30T23:50:00+00:00",
            4711,
            "10.0.0.0/16",
            ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            "mynet",
            new Protection11.Builder(
                false
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            Arrays.asList(
                new Route.Builder(
                    "10.100.1.0/24",
                    "10.0.1.1"
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            ),
            Arrays.asList(
                42
            ),
            Arrays.asList(
                new Subnet.Builder(
                    "10.0.0.1",
                    "eu-central",
                    Type42.CLOUD
                )
                .ipRange("10.0.1.0/24")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            )
        )
        .loadBalancers(Arrays.asList(
                42
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
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
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



