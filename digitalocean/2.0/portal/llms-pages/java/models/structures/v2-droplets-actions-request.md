# V2 Droplets Actions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVxdWVzdA

Specifies the action that will be taken on the Droplet.

*This model accepts additional fields of type Object.*


# Class Name

`V2DropletsActionsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-12.md) | Required | The type of action to initiate for the Droplet. | Type12 getType() | setType(Type12 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Type12;
import com.digitalocean.api.models.V2DropletsActionsRequest;
import java.io.IOException;

V2DropletsActionsRequest v2DropletsActionsRequest = new V2DropletsActionsRequest.Builder(
    Type12.REBOOT
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



