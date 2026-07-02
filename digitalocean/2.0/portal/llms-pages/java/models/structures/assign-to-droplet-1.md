# Assign to Droplet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkFzc2lnbiUyNTIwdG8lMjUyMERyb3BsZXQx

*This model accepts additional fields of type Object.*


# Class Name

`AssignToDroplet1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DropletId` | `int` | Required | The ID of the Droplet that the reserved IP will be assigned to. | int getDropletId() | setDropletId(int dropletId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AssignToDroplet1;
import java.io.IOException;

AssignToDroplet1 assignToDroplet1 = new AssignToDroplet1.Builder(
    2457247
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



