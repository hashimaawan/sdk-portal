# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0


# Class Name

`CreateFloatingIPRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | - | String getDescription() | setDescription(String description) |
| `HomeLocation` | `String` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. | String getHomeLocation() | setHomeLocation(String homeLocation) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Server` | `Integer` | Optional | Server to assign the Floating IP to | Integer getServer() | setServer(Integer server) |
| `Type` | [`Type17Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/type-17.md) | Required | Floating IP type | Type17Enum getType() | setType(Type17Enum type) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreateFloatingIPRequest;
import cloud.hetzner.api.models.Type17Enum;
import java.io.IOException;

CreateFloatingIPRequest createFloatingIPRequest = new CreateFloatingIPRequest.Builder(
    Type17Enum.IPV4
)
.description("Web Frontend")
.homeLocation("fsn1")
.labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
.name("Web Frontend")
.server(42)
.build();
```



