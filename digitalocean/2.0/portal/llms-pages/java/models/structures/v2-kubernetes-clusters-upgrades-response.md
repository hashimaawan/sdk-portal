# V2 Kubernetes Clusters Upgrades Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXBncmFkZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersUpgradesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AvailableUpgradeVersions` | [`List<AvailableUpgradeVersion>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/available-upgrade-version.md) | Optional | - | List<AvailableUpgradeVersion> getAvailableUpgradeVersions() | setAvailableUpgradeVersions(List<AvailableUpgradeVersion> availableUpgradeVersions) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AvailableUpgradeVersion;
import com.digitalocean.api.models.V2KubernetesClustersUpgradesResponse;
import java.io.IOException;
import java.util.Arrays;

V2KubernetesClustersUpgradesResponse v2KubernetesClustersUpgradesResponse = new V2KubernetesClustersUpgradesResponse.Builder()
    .availableUpgradeVersions(Arrays.asList(
        new AvailableUpgradeVersion.Builder()
            .kubernetesVersion("kubernetes_version0")
            .slug("slug2")
            .supportedFeatures(Arrays.asList(
                "supported_features3"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



