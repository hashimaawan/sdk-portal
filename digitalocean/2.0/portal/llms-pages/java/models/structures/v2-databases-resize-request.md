# V2 Databases Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesResizeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NumNodes` | `int` | Required | The number of nodes in the database cluster. Valid values are are 1-3. In addition to the primary node, up to two standby nodes may be added for highly available configurations. | int getNumNodes() | setNumNodes(int numNodes) |
| `Size` | `String` | Required | A slug identifier representing desired the size of the nodes in the database cluster. | String getSize() | setSize(String size) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2DatabasesResizeRequest;
import java.io.IOException;

V2DatabasesResizeRequest v2DatabasesResizeRequest = new V2DatabasesResizeRequest.Builder(
    3,
    "db-s-4vcpu-8gb"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



