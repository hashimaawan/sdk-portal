# Kubernetes Cluster User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVyVXNlcg

*This model accepts additional fields of type Object.*


# Class Name

`KubernetesClusterUser`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Groups` | `List<String>` | Optional | A list of in-cluster groups that the user belongs to. | List<String> getGroups() | setGroups(List<String> groups) |
| `Username` | `String` | Optional | The username for the cluster admin user. | String getUsername() | setUsername(String username) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.KubernetesClusterUser;
import java.io.IOException;
import java.util.Arrays;

KubernetesClusterUser kubernetesClusterUser = new KubernetesClusterUser.Builder()
    .groups(Arrays.asList(
        "k8saas:authenticated"
    ))
    .username("sammy@digitalocean.com")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



