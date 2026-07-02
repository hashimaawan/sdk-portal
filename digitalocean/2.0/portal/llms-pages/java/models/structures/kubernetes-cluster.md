# Kubernetes Cluster

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVy

*This model accepts additional fields of type Object.*


# Class Name

`KubernetesCluster`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AutoUpgrade` | `Boolean` | Optional | A boolean value indicating whether the cluster will be automatically upgraded to new patch releases during its maintenance window.<br><br>**Default**: `false` | Boolean getAutoUpgrade() | setAutoUpgrade(Boolean autoUpgrade) |
| `ClusterSubnet` | `String` | Optional, Read-only | The range of IP addresses in the overlay network of the Kubernetes cluster in CIDR notation. | String getClusterSubnet() | setClusterSubnet(String clusterSubnet) |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the Kubernetes cluster was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `Endpoint` | `String` | Optional, Read-only | The base URL of the API server on the Kubernetes master node. | String getEndpoint() | setEndpoint(String endpoint) |
| `Ha` | `Boolean` | Optional | A boolean value indicating whether the control plane is run in a highly available configuration in the cluster. Highly available control planes incur less downtime. The property cannot be disabled.<br><br>**Default**: `false` | Boolean getHa() | setHa(Boolean ha) |
| `Id` | `UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a Kubernetes cluster. | UUID getId() | setId(UUID id) |
| `Ipv4` | `String` | Optional, Read-only | The public IPv4 address of the Kubernetes master node. This will not be set if high availability is configured on the cluster (v1.21+) | String getIpv4() | setIpv4(String ipv4) |
| `MaintenancePolicy` | [`MaintenancePolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/maintenance-policy.md) | Optional | An object specifying the maintenance window policy for the Kubernetes cluster. | MaintenancePolicy getMaintenancePolicy() | setMaintenancePolicy(MaintenancePolicy maintenancePolicy) |
| `Name` | `String` | Required | A human-readable name for a Kubernetes cluster. | String getName() | setName(String name) |
| `NodePools` | [`List<NodePool>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/node-pool.md) | Required | An object specifying the details of the worker nodes available to the Kubernetes cluster. | List<NodePool> getNodePools() | setNodePools(List<NodePool> nodePools) |
| `Region` | `String` | Required | The slug identifier for the region where the Kubernetes cluster is located. | String getRegion() | setRegion(String region) |
| `RegistryEnabled` | `Boolean` | Optional, Read-only | A read-only boolean value indicating if a container registry is integrated with the cluster. | Boolean getRegistryEnabled() | setRegistryEnabled(Boolean registryEnabled) |
| `ServiceSubnet` | `String` | Optional, Read-only | The range of assignable IP addresses for services running in the Kubernetes cluster in CIDR notation. | String getServiceSubnet() | setServiceSubnet(String serviceSubnet) |
| `Status` | [`Status11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/status-11.md) | Optional, Read-only | An object containing a `state` attribute whose value is set to a string indicating the current status of the cluster. | Status11 getStatus() | setStatus(Status11 status) |
| `SurgeUpgrade` | `Boolean` | Optional | A boolean value indicating whether surge upgrade is enabled/disabled for the cluster. Surge upgrade makes cluster upgrades fast and reliable by bringing up new nodes before destroying the outdated nodes.<br><br>**Default**: `false` | Boolean getSurgeUpgrade() | setSurgeUpgrade(Boolean surgeUpgrade) |
| `Tags` | `List<String>` | Optional | An array of tags applied to the Kubernetes cluster. All clusters are automatically tagged `k8s` and `k8s:$K8S_CLUSTER_ID`. | List<String> getTags() | setTags(List<String> tags) |
| `UpdatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the Kubernetes cluster was last updated. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `Version` | `String` | Required | The slug identifier for the version of Kubernetes used for the cluster. If set to a minor version (e.g. "1.14"), the latest version within it will be used (e.g. "1.14.6-do.1"); if set to "latest", the latest published version will be used. See the `/v2/kubernetes/options` endpoint to find all currently available versions. | String getVersion() | setVersion(String version) |
| `VpcUuid` | `UUID` | Optional | A string specifying the UUID of the VPC to which the Kubernetes cluster is assigned. | UUID getVpcUuid() | setVpcUuid(UUID vpcUuid) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.KubernetesCluster;
import com.digitalocean.api.models.NodePool;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

KubernetesCluster kubernetesCluster = new KubernetesCluster.Builder(
    "prod-cluster-01",
    Arrays.asList(
        new NodePool.Builder(
            "s-1vcpu-2gb",
            3,
            "frontend-pool"
        )
        .autoScale(true)
        .id(UUID.fromString("cdda885e-7663-40c8-bc74-3a036c66545d"))
        .labels(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .maxNodes(6)
        .minNodes(3)
        .tags(Arrays.asList(
                "k8s",
                "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
                "k8s-worker",
                "production",
                "web-team"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    "nyc1",
    "1.18.6-do.0"
)
.autoUpgrade(true)
.clusterSubnet("10.244.0.0/16")
.createdAt(DateTimeHelper.fromRfc8601DateTime("2018-11-15T16:00:11Z"))
.endpoint("https://bd5f5959-5e1e-4205-a714-a914373942af.k8s.ondigitalocean.com")
.ha(true)
.id(UUID.fromString("bd5f5959-5e1e-4205-a714-a914373942af"))
.ipv4("68.183.121.157")
.registryEnabled(true)
.serviceSubnet("10.245.0.0/16")
.surgeUpgrade(true)
.tags(Arrays.asList(
        "k8s",
        "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
        "production",
        "web-team"
    ))
.updatedAt(DateTimeHelper.fromRfc8601DateTime("2018-11-15T16:00:11Z"))
.vpcUuid(UUID.fromString("c33931f2-a26a-4e61-b85c-4e95a2ec431b"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



