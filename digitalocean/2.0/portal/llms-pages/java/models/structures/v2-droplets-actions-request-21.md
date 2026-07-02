# V2 Droplets Actions Request 21

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVxdWVzdDIx

*This model accepts additional fields of type Object.*


# Class Name

`V2DropletsActionsRequest21`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-12.md) | Required | The type of action to initiate for the Droplet. | Type12 getType() | setType(Type12 type) |
| `Disk` | `Boolean` | Optional | When `true`, the Droplet's disk will be resized in addition to its RAM and CPU. This is a permanent change and cannot be reversed as a Droplet's disk size cannot be decreased. | Boolean getDisk() | setDisk(Boolean disk) |
| `Size` | `String` | Optional | The slug identifier for the size to which you wish to resize the Droplet. | String getSize() | setSize(String size) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Type12;
import com.digitalocean.api.models.V2DropletsActionsRequest21;
import java.io.IOException;

V2DropletsActionsRequest21 v2DropletsActionsRequest21 = new V2DropletsActionsRequest21.Builder(
    Type12.REBOOT
)
.disk(true)
.size("s-2vcpu-2gb")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



