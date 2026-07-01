# Floating Ips Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNl


# Class Name

`FloatingIpsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FloatingIps` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/floating-ip.md) | Required | - | List<FloatingIp> getFloatingIps() | setFloatingIps(List<FloatingIp> floatingIps) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |


# Example

```java
import cloud.hetzner.api.models.DnsPtr;
import cloud.hetzner.api.models.FloatingIp;
import cloud.hetzner.api.models.FloatingIpsResponse;
import cloud.hetzner.api.models.HomeLocation;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Type16Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

FloatingIpsResponse floatingIpsResponse = new FloatingIpsResponse.Builder(
    Arrays.asList(
        new FloatingIp.Builder(
            false,
            "2016-01-30T23:55:00+00:00",
            "this describes my resource",
            Arrays.asList(
                new DnsPtr.Builder(
                    "server.example.com",
                    "2001:db8::1"
                )
                .build()
            ),
            new HomeLocation.Builder(
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
            42,
            "131.232.99.1",
            new LinkedHashMap<String, String>() {{
                put("key0", "labels2");
            }},
            "my-resource",
            new Protection.Builder(
                false
            )
            .build(),
            42,
            Type16Enum.IPV4
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



