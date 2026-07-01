# Floating Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`FloatingIpsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Optional | - | Action getAction() | setAction(Action action) |
| `FloatingIp` | [`FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/floating-ip.md) | Required | - | FloatingIp getFloatingIp() | setFloatingIp(FloatingIp floatingIp) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.DnsPtr;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.FloatingIp;
import cloud.hetzner.api.models.FloatingIpsResponse1;
import cloud.hetzner.api.models.HomeLocation;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.Status;
import cloud.hetzner.api.models.Type16;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

FloatingIpsResponse1 floatingIpsResponse1 = new FloatingIpsResponse1.Builder(
    new FloatingIp.Builder(
        false,
        "2016-01-30T23:55:00+00:00",
        "this describes my resource",
        Arrays.asList(
            new DnsPtr.Builder(
                "server.example.com",
                "2001:db8::1"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
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
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
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
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        42,
        Type16.IPV4
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.action(new Action.Builder(
        "command6",
        new Error.Builder(
            "code2",
            "message4"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "finished0",
        238,
        143.26D,
        Arrays.asList(
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        "started8",
        Status.RUNNING
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



