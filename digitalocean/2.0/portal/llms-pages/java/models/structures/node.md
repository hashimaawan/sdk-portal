# Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk5vZGU

*This model accepts additional fields of type Object.*


# Class Name

`Node`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `DropletId` | `String` | Optional | The ID of the Droplet used for the worker node. | String getDropletId() | setDropletId(String dropletId) |
| `Id` | `UUID` | Optional | A unique ID that can be used to identify and reference the node. | UUID getId() | setId(UUID id) |
| `Name` | `String` | Optional | An automatically generated, human-readable name for the node. | String getName() | setName(String name) |
| `Status` | [`Status10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/status-10.md) | Optional | An object containing a `state` attribute whose value is set to a string indicating the current status of the node. | Status10 getStatus() | setStatus(Status10 status) |
| `UpdatedAt` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was last updated. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Node;
import com.digitalocean.api.models.State1;
import com.digitalocean.api.models.Status10;
import java.io.IOException;
import java.util.UUID;

Node node = new Node.Builder()
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2018-11-15T16:00:11Z"))
    .dropletId("205545370")
    .id(UUID.fromString("e78247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f"))
    .name("adoring-newton-3niq")
    .status(new Status10.Builder()
        .state(State1.PROVISIONING)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .updatedAt(DateTimeHelper.fromRfc8601DateTime("2018-11-15T16:00:11Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



