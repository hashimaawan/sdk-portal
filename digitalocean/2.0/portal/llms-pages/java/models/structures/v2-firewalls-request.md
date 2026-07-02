# V2 Firewalls Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2FirewallsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `DropletIds` | `List<Integer>` | Optional | An array containing the IDs of the Droplets assigned to the firewall. | List<Integer> getDropletIds() | setDropletIds(List<Integer> dropletIds) |
| `Id` | `String` | Optional, Read-only | A unique ID that can be used to identify and reference a firewall. | String getId() | setId(String id) |
| `Name` | `String` | Required | A human-readable name for a firewall. The name must begin with an alphanumeric character. Subsequent characters must either be alphanumeric characters, a period (.), or a dash (-).<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\.-]+$` | String getName() | setName(String name) |
| `PendingChanges` | [`List<PendingChange>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/pending-change.md) | Optional, Read-only | An array of objects each containing the fields "droplet_id", "removing", and "status". It is provided to detail exactly which Droplets are having their security policies updated. When empty, all changes have been successfully applied. | List<PendingChange> getPendingChanges() | setPendingChanges(List<PendingChange> pendingChanges) |
| `Status` | [`Status9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-9.md) | Optional, Read-only | A status string indicating the current state of the firewall. This can be "waiting", "succeeded", or "failed". | Status9 getStatus() | setStatus(Status9 status) |
| `Tags` | `List<String>` | Optional | - | List<String> getTags() | setTags(List<String> tags) |
| `InboundRules` | [`List<InboundRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/inbound-rule.md) | Required | - | List<InboundRule> getInboundRules() | setInboundRules(List<InboundRule> inboundRules) |
| `OutboundRules` | [`List<OutboundRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/outbound-rule.md) | Required | - | List<OutboundRule> getOutboundRules() | setOutboundRules(List<OutboundRule> outboundRules) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Destinations;
import com.digitalocean.api.models.InboundRule;
import com.digitalocean.api.models.OutboundRule;
import com.digitalocean.api.models.PendingChange;
import com.digitalocean.api.models.Protocol;
import com.digitalocean.api.models.Sources;
import com.digitalocean.api.models.Status9;
import com.digitalocean.api.models.V2FirewallsRequest;
import java.io.IOException;
import java.util.Arrays;

V2FirewallsRequest v2FirewallsRequest = new V2FirewallsRequest.Builder(
    "firewall",
    Arrays.asList(
        new InboundRule.Builder(
            "8000",
            Protocol.TCP,
            new Sources.Builder()
                .addresses(Arrays.asList(
                    "1.2.3.4",
                    "18.0.0.0/8"
                ))
                .dropletIds(Arrays.asList(
                    8043964
                ))
                .kubernetesIds(Arrays.asList(
                    "41b74c5d-9bd0-5555-5555-a57c495b81a3"
                ))
                .loadBalancerUids(Arrays.asList(
                    "4de7ac8b-495b-4884-9a69-1050c6793cd6"
                ))
                .tags(Arrays.asList(
                    "tags1",
                    "tags2",
                    "tags3"
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    Arrays.asList(
        new OutboundRule.Builder(
            "8000",
            Protocol.TCP,
            new Destinations.Builder()
                .addresses(Arrays.asList(
                    "1.2.3.4",
                    "18.0.0.0/8"
                ))
                .dropletIds(Arrays.asList(
                    8043964
                ))
                .kubernetesIds(Arrays.asList(
                    "41b74c5d-9bd0-5555-5555-a57c495b81a3"
                ))
                .loadBalancerUids(Arrays.asList(
                    "4de7ac8b-495b-4884-9a69-1050c6793cd6"
                ))
                .tags(Arrays.asList(
                    "tags7",
                    "tags8",
                    "tags9"
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.createdAt(DateTimeHelper.fromRfc8601DateTime("2020-05-23T21:24:00Z"))
.dropletIds(Arrays.asList(
        8043964
    ))
.id("bb4b2611-3d72-467b-8602-280330ecd65c")
.pendingChanges(Arrays.asList(
        new PendingChange.Builder()
            .dropletId(8043964)
            .removing(false)
            .status("waiting")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.status(Status9.WAITING)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



