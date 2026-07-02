# V2 Kubernetes Clusters User Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXNlciUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersUserResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `KubernetesClusterUser` | [`KubernetesClusterUser`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/kubernetes-cluster-user.md) | Optional | - | KubernetesClusterUser getKubernetesClusterUser() | setKubernetesClusterUser(KubernetesClusterUser kubernetesClusterUser) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.KubernetesClusterUser;
import com.digitalocean.api.models.V2KubernetesClustersUserResponse;
import java.io.IOException;
import java.util.Arrays;

V2KubernetesClustersUserResponse v2KubernetesClustersUserResponse = new V2KubernetesClustersUserResponse.Builder()
    .kubernetesClusterUser(new KubernetesClusterUser.Builder()
        .groups(Arrays.asList(
            "groups8"
        ))
        .username("username6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



