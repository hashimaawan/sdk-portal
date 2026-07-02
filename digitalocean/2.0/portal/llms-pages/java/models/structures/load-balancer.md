# Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcg

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancer`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | The ID of a resource associated with a Kubernetes cluster. | String getId() | setId(String id) |
| `Name` | `String` | Optional | The name of a resource associated with a Kubernetes cluster. | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.LoadBalancer;
import java.io.IOException;

LoadBalancer loadBalancer = new LoadBalancer.Builder()
    .id("edb0478d-7436-11ea-86e6-0a58ac144b91")
    .name("volume-001")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



