# Floating Ips Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMg


# Class Name

`FloatingIpsResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FloatingIp` | [`FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/floating-ip.md) | Required | - | FloatingIp getFloatingIp() | setFloatingIp(FloatingIp floatingIp) |


# Example

```java
import cloud.hetzner.api.models.DnsPtr;
import cloud.hetzner.api.models.FloatingIp;
import cloud.hetzner.api.models.FloatingIpsResponse2;
import cloud.hetzner.api.models.HomeLocation;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Type16Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

FloatingIpsResponse2 floatingIpsResponse2 = new FloatingIpsResponse2.Builder(
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
            put("key0", "labels4");
            put("key1", "labels3");
            put("key2", "labels2");
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
.build();
```



