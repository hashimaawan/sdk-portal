# V2 Floating Ips Actions Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGbG9hdGluZyUyNTIwSXBzJTI1MjBBY3Rpb25zJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2FloatingIpsActionsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/action-2.md) | Optional | - | Action2 getAction() | setAction(Action2 action) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Action2;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.Status1;
import com.digitalocean.api.models.V2FloatingIpsActionsResponse1;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2FloatingIpsActionsResponse1 v2FloatingIpsActionsResponse1 = new V2FloatingIpsActionsResponse1.Builder()
    .action(new Action2.Builder()
        .completedAt(DateTimeHelper.fromRfc8601DateTime("2015-11-12T17:51:14Z"))
        .id(72531856)
        .region(new Region.Builder(
            true,
            Arrays.asList(
                "private_networking",
                "backups",
                "ipv6",
                "metadata"
            ),
            "New York 3",
            Arrays.asList(
                "s-1vcpu-1gb",
                "s-1vcpu-2gb",
                "s-1vcpu-3gb",
                "s-2vcpu-2gb",
                "s-3vcpu-1gb",
                "s-2vcpu-4gb",
                "s-4vcpu-8gb",
                "s-6vcpu-16gb",
                "s-8vcpu-32gb",
                "s-12vcpu-48gb",
                "s-16vcpu-64gb",
                "s-20vcpu-96gb",
                "s-24vcpu-128gb",
                "s-32vcpu-192gb"
            ),
            "nyc3"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
        .regionSlug("nyc3")
        .resourceId(758604968)
        .resourceType("floating_ip")
        .startedAt(DateTimeHelper.fromRfc8601DateTime("2015-11-12T17:51:03Z"))
        .status(Status1.COMPLETED)
        .type("assign_ip")
        .projectId(UUID.fromString("746c6152-2fa2-11ed-92d3-27aaa54e4988"))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



