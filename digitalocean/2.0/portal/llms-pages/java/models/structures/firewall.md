# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkZpcmV3YWxs

*This model accepts additional fields of type Object.*


# Class Name

`Firewall`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `DropletIds` | `List<Integer>` | Optional | An array containing the IDs of the Droplets assigned to the firewall. | List<Integer> getDropletIds() | setDropletIds(List<Integer> dropletIds) |
| `Id` | `String` | Optional, Read-only | A unique ID that can be used to identify and reference a firewall. | String getId() | setId(String id) |
| `Name` | `String` | Optional | A human-readable name for a firewall. The name must begin with an alphanumeric character. Subsequent characters must either be alphanumeric characters, a period (.), or a dash (-).<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\.-]+$` | String getName() | setName(String name) |
| `PendingChanges` | [`List<PendingChange>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/pending-change.md) | Optional, Read-only | An array of objects each containing the fields "droplet_id", "removing", and "status". It is provided to detail exactly which Droplets are having their security policies updated. When empty, all changes have been successfully applied. | List<PendingChange> getPendingChanges() | setPendingChanges(List<PendingChange> pendingChanges) |
| `Status` | [`Status9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-9.md) | Optional, Read-only | A status string indicating the current state of the firewall. This can be "waiting", "succeeded", or "failed". | Status9 getStatus() | setStatus(Status9 status) |
| `Tags` | `List<String>` | Optional | - | List<String> getTags() | setTags(List<String> tags) |
| `InboundRules` | [`List<InboundRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/inbound-rule.md) | Optional | - | List<InboundRule> getInboundRules() | setInboundRules(List<InboundRule> inboundRules) |
| `OutboundRules` | [`List<OutboundRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/outbound-rule.md) | Optional | - | List<OutboundRule> getOutboundRules() | setOutboundRules(List<OutboundRule> outboundRules) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Firewall;
import com.digitalocean.api.models.PendingChange;
import com.digitalocean.api.models.Status9;
import java.io.IOException;
import java.util.Arrays;

Firewall firewall = new Firewall.Builder()
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2020-05-23T21:24:00Z"))
    .dropletIds(Arrays.asList(
        8043964
    ))
    .id("bb4b2611-3d72-467b-8602-280330ecd65c")
    .name("firewall")
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



