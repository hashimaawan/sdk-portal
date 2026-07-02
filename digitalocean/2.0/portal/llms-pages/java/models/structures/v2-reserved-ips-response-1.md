# V2 Reserved Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBSZXNlcnZlZCUyNTIwSXBzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2ReservedIpsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Links` | [`Links3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links-3.md) | Optional | - | Links3 getLinks() | setLinks(Links3 links) |
| `ReservedIp` | [`ReservedIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/reserved-ip.md) | Optional | - | ReservedIp getReservedIp() | setReservedIp(ReservedIp reservedIp) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Action1;
import com.digitalocean.api.models.Links3;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.ReservedIp;
import com.digitalocean.api.models.V2ReservedIpsResponse1;
import com.digitalocean.api.models.containers.ReservedIpDroplet;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2ReservedIpsResponse1 v2ReservedIpsResponse1 = new V2ReservedIpsResponse1.Builder()
    .links(new Links3.Builder()
        .actions(Arrays.asList(
            new Action1.Builder()
                .href("href0")
                .id(154)
                .rel("rel4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
        .droplets(Arrays.asList(
            new Action1.Builder()
                .href("href2")
                .id(232)
                .rel("rel6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new Action1.Builder()
                .href("href2")
                .id(232)
                .rel("rel6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .reservedIp(new ReservedIp.Builder()
        .droplet(ReservedIpDroplet.fromObject(
            ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
        ))
        .ip("ip6")
        .locked(false)
        .projectId(UUID.fromString("00002548-0000-0000-0000-000000000000"))
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



