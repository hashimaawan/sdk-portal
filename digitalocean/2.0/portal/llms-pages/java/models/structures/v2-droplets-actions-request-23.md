# V2 Droplets Actions Request 23

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVxdWVzdDIz

*This model accepts additional fields of type Object.*


# Class Name

`V2DropletsActionsRequest23`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-12.md) | Required | The type of action to initiate for the Droplet. | Type12 getType() | setType(Type12 type) |
| `Name` | `String` | Optional | The new name for the Droplet. | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Type12;
import com.digitalocean.api.models.V2DropletsActionsRequest23;
import java.io.IOException;

V2DropletsActionsRequest23 v2DropletsActionsRequest23 = new V2DropletsActionsRequest23.Builder(
    Type12.REBOOT
)
.name("nifty-new-name")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



