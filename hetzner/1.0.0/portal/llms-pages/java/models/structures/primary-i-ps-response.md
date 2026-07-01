# Primary I Ps Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaW1hcnlJUHNSZXNwb25zZQ


# Class Name

`PrimaryIPsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |
| `PrimaryIps` | [`List<PrimaryIP1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/primary-ip-1.md) | Required | - | List<PrimaryIP1> getPrimaryIps() | setPrimaryIps(List<PrimaryIP1> primaryIps) |


# Example

```java
import cloud.hetzner.api.models.Datacenter2;
import cloud.hetzner.api.models.DnsPtr;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.PrimaryIP1;
import cloud.hetzner.api.models.PrimaryIPsResponse;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.ServerTypes;
import cloud.hetzner.api.models.Type50Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

PrimaryIPsResponse primaryIPsResponse = new PrimaryIPsResponse.Builder(
    Arrays.asList(
        new PrimaryIP1.Builder(
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
                .build()
            )
            .build(),
            Arrays.asList(
                new DnsPtr.Builder(
                    "server.example.com",
                    "2001:db8::1"
                )
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
            .build(),
            Type50Enum.IPV4
        )
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



