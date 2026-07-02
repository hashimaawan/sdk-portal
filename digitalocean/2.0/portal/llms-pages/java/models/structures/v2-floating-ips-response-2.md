# V2 Floating Ips Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGbG9hdGluZyUyNTIwSXBzJTI1MjBSZXNwb25zZTI

*This model accepts additional fields of type Object.*


# Class Name

`V2FloatingIpsResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FloatingIp` | [`FloatingIp1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/floating-ip-1.md) | Optional | - | FloatingIp1 getFloatingIp() | setFloatingIp(FloatingIp1 floatingIp) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.FloatingIp1;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.V2FloatingIpsResponse2;
import com.digitalocean.api.models.containers.FloatingIp1Droplet;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2FloatingIpsResponse2 v2FloatingIpsResponse2 = new V2FloatingIpsResponse2.Builder()
    .floatingIp(new FloatingIp1.Builder()
        .droplet(FloatingIp1Droplet.fromObject(
            ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
        ))
        .ip("ip2")
        .locked(false)
        .projectId(UUID.fromString("0000167e-0000-0000-0000-000000000000"))
        .region(new Region.Builder(
            false,
            Arrays.asList(
                "features7",
                "features8",
                "features9"
            ),
            "name6",
            Arrays.asList(
                "sizes6"
            ),
            "slug0"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



