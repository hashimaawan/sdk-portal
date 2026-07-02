# V2 Kubernetes Clusters Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing the IDs of resources to be destroyed along with their associated with a Kubernetes cluster.

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LoadBalancers` | `List<String>` | Optional | A list of IDs for associated load balancers to destroy along with the cluster. | List<String> getLoadBalancers() | setLoadBalancers(List<String> loadBalancers) |
| `VolumeSnapshots` | `List<String>` | Optional | A list of IDs for associated volume snapshots to destroy along with the cluster. | List<String> getVolumeSnapshots() | setVolumeSnapshots(List<String> volumeSnapshots) |
| `Volumes` | `List<String>` | Optional | A list of IDs for associated volumes to destroy along with the cluster. | List<String> getVolumes() | setVolumes(List<String> volumes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest;
import java.io.IOException;
import java.util.Arrays;

V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest v2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest = new V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest.Builder()
    .loadBalancers(Arrays.asList(
        "4de7ac8b-495b-4884-9a69-1050c6793cd6"
    ))
    .volumeSnapshots(Arrays.asList(
        "edb0478d-7436-11ea-86e6-0a58ac144b91"
    ))
    .volumes(Arrays.asList(
        "ba49449a-7435-11ea-b89e-0a58ac14480f"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



