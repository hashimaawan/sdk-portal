# Pending Change

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlBlbmRpbmdDaGFuZ2U

*This model accepts additional fields of type Object.*


# Class Name

`PendingChange`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DropletId` | `Integer` | Optional | - | Integer getDropletId() | setDropletId(Integer dropletId) |
| `Removing` | `Boolean` | Optional | - | Boolean getRemoving() | setRemoving(Boolean removing) |
| `Status` | `String` | Optional | - | String getStatus() | setStatus(String status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.PendingChange;
import java.io.IOException;

PendingChange pendingChange = new PendingChange.Builder()
    .dropletId(8043964)
    .removing(false)
    .status("waiting")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



