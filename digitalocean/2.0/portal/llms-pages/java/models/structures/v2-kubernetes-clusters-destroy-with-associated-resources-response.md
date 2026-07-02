# V2 Kubernetes Clusters Destroy with Associated Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

An object containing the IDs of resources associated with a Kubernetes cluster.

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersDestroyWithAssociatedResourcesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LoadBalancers` | [`List<LoadBalancer>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated load balancers that can be destroyed along with the cluster. | List<LoadBalancer> getLoadBalancers() | setLoadBalancers(List<LoadBalancer> loadBalancers) |
| `VolumeSnapshots` | [`List<LoadBalancer>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated volume snapshots that can be destroyed along with the cluster. | List<LoadBalancer> getVolumeSnapshots() | setVolumeSnapshots(List<LoadBalancer> volumeSnapshots) |
| `Volumes` | [`List<LoadBalancer>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated volumes that can be destroyed along with the cluster. | List<LoadBalancer> getVolumes() | setVolumes(List<LoadBalancer> volumes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.LoadBalancer;
import com.digitalocean.api.models.V2KubernetesClustersDestroyWithAssociatedResourcesResponse;
import java.io.IOException;
import java.util.Arrays;

V2KubernetesClustersDestroyWithAssociatedResourcesResponse v2KubernetesClustersDestroyWithAssociatedResourcesResponse = new V2KubernetesClustersDestroyWithAssociatedResourcesResponse.Builder()
    .loadBalancers(Arrays.asList(
        new LoadBalancer.Builder()
            .id("4de7ac8b-495b-4884-9a69-1050c6793cd6")
            .name("lb-001")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .volumeSnapshots(Arrays.asList(
        new LoadBalancer.Builder()
            .id("edb0478d-7436-11ea-86e6-0a58ac144b91")
            .name("snapshot-001")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .volumes(Arrays.asList(
        new LoadBalancer.Builder()
            .id("ba49449a-7435-11ea-b89e-0a58ac14480f")
            .name("volume-001")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



