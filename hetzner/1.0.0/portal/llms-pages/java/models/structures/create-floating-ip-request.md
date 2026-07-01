# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`CreateFloatingIpRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | - | String getDescription() | setDescription(String description) |
| `HomeLocation` | `String` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. | String getHomeLocation() | setHomeLocation(String homeLocation) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Server` | `Integer` | Optional | Server to assign the Floating IP to | Integer getServer() | setServer(Integer server) |
| `Type` | [`Type17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-17.md) | Required | Floating IP type | Type17 getType() | setType(Type17 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreateFloatingIpRequest;
import cloud.hetzner.api.models.Type17;
import java.io.IOException;

CreateFloatingIpRequest createFloatingIpRequest = new CreateFloatingIpRequest.Builder(
    Type17.IPV4
)
.description("Web Frontend")
.homeLocation("fsn1")
.labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
.name("Web Frontend")
.server(42)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



