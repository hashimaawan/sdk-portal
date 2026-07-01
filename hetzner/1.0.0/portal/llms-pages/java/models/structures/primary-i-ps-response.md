# Primary I Ps Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaW1hcnlJUHNSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`PrimaryIPsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |
| `PrimaryIps` | [`List<PrimaryIp1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/primary-ip-1.md) | Required | - | List<PrimaryIp1> getPrimaryIps() | setPrimaryIps(List<PrimaryIp1> primaryIps) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Datacenter2;
import cloud.hetzner.api.models.DnsPtr;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.PrimaryIPsResponse;
import cloud.hetzner.api.models.PrimaryIp1;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.ServerTypes;
import cloud.hetzner.api.models.Type50;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

PrimaryIPsResponse primaryIPsResponse = new PrimaryIPsResponse.Builder(
    Arrays.asList(
        new PrimaryIp1.Builder(
            17,
            "server",
            true,
            false,
            "2016-01-30T23:55:00+00:00",
            new Datacenter2.Builder(
                "Falkenstein DC Park 8",
                42,
                new Location.Builder(
                    "Falkenstein",
                    "DE",
                    "Falkenstein DC Park 1",
                    1D,
                    50.47612D,
                    12.370071D,
                    "fsn1",
                    "eu-central"
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
                "fsn1-dc8",
                new ServerTypes.Builder(
                    Arrays.asList(
                        1D,
                        2D,
                        3D
                    ),
                    Arrays.asList(
                        1D,
                        2D,
                        3D
                    ),
                    Arrays.asList(
                        1D,
                        2D,
                        3D
                    )
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            Arrays.asList(
                new DnsPtr.Builder(
                    "server.example.com",
                    "2001:db8::1"
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            ),
            42,
            "131.232.99.1",
            new LinkedHashMap<String, String>() {{
                put("key0", "labels2");
                put("key1", "labels3");
                put("key2", "labels4");
            }},
            "my-resource",
            new Protection.Builder(
                false
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            Type50.IPV4
        )
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



