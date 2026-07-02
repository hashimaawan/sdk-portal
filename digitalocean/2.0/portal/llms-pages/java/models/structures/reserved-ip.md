# Reserved Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlc2VydmVkSXA

*This model accepts additional fields of type Object.*


# Class Name

`ReservedIp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Droplet` | [`ReservedIpDroplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/oneof-anyof-definitions/reserved-ip-droplet.md) | Optional | This is a container for any-of cases. | ReservedIpDroplet getDroplet() | setDroplet(ReservedIpDroplet droplet) |
| `Ip` | `String` | Optional | The public IP address of the reserved IP. It also serves as its identifier. | String getIp() | setIp(String ip) |
| `Locked` | `Boolean` | Optional | A boolean value indicating whether or not the reserved IP has pending actions preventing new ones from being submitted. | Boolean getLocked() | setLocked(Boolean locked) |
| `ProjectId` | `UUID` | Optional | The UUID of the project to which the reserved IP currently belongs. | UUID getProjectId() | setProjectId(UUID projectId) |
| `Region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/region.md) | Optional | - | Region getRegion() | setRegion(Region region) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.ReservedIp;
import com.digitalocean.api.models.containers.ReservedIpDroplet;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

ReservedIp reservedIp = new ReservedIp.Builder()
    .droplet(ReservedIpDroplet.fromObject(
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
    ))
    .ip("45.55.96.47")
    .locked(true)
    .projectId(UUID.fromString("746c6152-2fa2-11ed-92d3-27aaa54e4988"))
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
    .build();
```



