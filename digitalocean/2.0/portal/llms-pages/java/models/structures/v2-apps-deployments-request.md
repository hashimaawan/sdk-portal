# V2 Apps Deployments Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBEZXBsb3ltZW50cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsDeploymentsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ForceBuild` | `Boolean` | Optional | - | Boolean getForceBuild() | setForceBuild(Boolean forceBuild) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2AppsDeploymentsRequest;
import java.io.IOException;

V2AppsDeploymentsRequest v2AppsDeploymentsRequest = new V2AppsDeploymentsRequest.Builder()
    .forceBuild(true)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



