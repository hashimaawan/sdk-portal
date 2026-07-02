# V2 Droplets Actions Request 22

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVxdWVzdDIy

*This model accepts additional fields of type Object.*


# Class Name

`V2DropletsActionsRequest22`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-12.md) | Required | The type of action to initiate for the Droplet. | Type12 getType() | setType(Type12 type) |
| `Image` | [`V2DropletsActionsRequest22Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/oneof-anyof-definitions/v2-droplets-actions-request-22-image.md) | Optional | This is a container for one-of cases. | V2DropletsActionsRequest22Image getImage() | setImage(V2DropletsActionsRequest22Image image) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Type12;
import com.digitalocean.api.models.V2DropletsActionsRequest22;
import com.digitalocean.api.models.containers.V2DropletsActionsRequest22Image;
import java.io.IOException;

V2DropletsActionsRequest22 v2DropletsActionsRequest22 = new V2DropletsActionsRequest22.Builder(
    Type12.REBOOT
)
.image(V2DropletsActionsRequest22Image.fromString(
        "ubuntu-20-04-x64"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



