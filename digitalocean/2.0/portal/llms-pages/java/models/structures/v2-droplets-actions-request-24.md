# V2 Droplets Actions Request 24

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVxdWVzdDI0

*This model accepts additional fields of type Object.*


# Class Name

`V2DropletsActionsRequest24`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-12.md) | Required | The type of action to initiate for the Droplet. | Type12 getType() | setType(Type12 type) |
| `Kernel` | `Integer` | Optional | A unique number used to identify and reference a specific kernel. | Integer getKernel() | setKernel(Integer kernel) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Type12;
import com.digitalocean.api.models.V2DropletsActionsRequest24;
import java.io.IOException;

V2DropletsActionsRequest24 v2DropletsActionsRequest24 = new V2DropletsActionsRequest24.Builder(
    Type12.REBOOT
)
.kernel(12389723)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



