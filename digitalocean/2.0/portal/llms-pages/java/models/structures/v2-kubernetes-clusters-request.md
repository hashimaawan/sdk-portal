# V2 Kubernetes Clusters Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AutoUpgrade` | `Boolean` | Optional | A boolean value indicating whether the cluster will be automatically upgraded to new patch releases during its maintenance window.<br><br>**Default**: `false` | Boolean getAutoUpgrade() | setAutoUpgrade(Boolean autoUpgrade) |
| `Ha` | `Boolean` | Optional | A boolean value indicating whether the control plane is run in a highly available configuration in the cluster. Highly available control planes incur less downtime. The property cannot be disabled.<br><br>**Default**: `false` | Boolean getHa() | setHa(Boolean ha) |
| `MaintenancePolicy` | [`MaintenancePolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/maintenance-policy.md) | Optional | An object specifying the maintenance window policy for the Kubernetes cluster. | MaintenancePolicy getMaintenancePolicy() | setMaintenancePolicy(MaintenancePolicy maintenancePolicy) |
| `Name` | `String` | Required | A human-readable name for a Kubernetes cluster. | String getName() | setName(String name) |
| `SurgeUpgrade` | `Boolean` | Optional | A boolean value indicating whether surge upgrade is enabled/disabled for the cluster. Surge upgrade makes cluster upgrades fast and reliable by bringing up new nodes before destroying the outdated nodes.<br><br>**Default**: `false` | Boolean getSurgeUpgrade() | setSurgeUpgrade(Boolean surgeUpgrade) |
| `Tags` | `List<String>` | Optional | An array of tags applied to the Kubernetes cluster. All clusters are automatically tagged `k8s` and `k8s:$K8S_CLUSTER_ID`. | List<String> getTags() | setTags(List<String> tags) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Day;
import com.digitalocean.api.models.MaintenancePolicy;
import com.digitalocean.api.models.V2KubernetesClustersRequest;
import java.io.IOException;
import java.util.Arrays;

V2KubernetesClustersRequest v2KubernetesClustersRequest = new V2KubernetesClustersRequest.Builder(
    "prod-cluster-01"
)
.autoUpgrade(true)
.ha(true)
.maintenancePolicy(new MaintenancePolicy.Builder()
        .day(Day.ANY)
        .duration("duration4")
        .startTime("start_time2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.surgeUpgrade(true)
.tags(Arrays.asList(
        "k8s",
        "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
        "production",
        "web-team"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



