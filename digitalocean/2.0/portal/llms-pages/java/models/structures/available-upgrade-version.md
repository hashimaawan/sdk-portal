# Available Upgrade Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkF2YWlsYWJsZVVwZ3JhZGVWZXJzaW9u

*This model accepts additional fields of type Object.*


# Class Name

`AvailableUpgradeVersion`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `KubernetesVersion` | `String` | Optional | The upstream version string for the version of Kubernetes provided by a given slug. | String getKubernetesVersion() | setKubernetesVersion(String kubernetesVersion) |
| `Slug` | `String` | Optional | The slug identifier for an available version of Kubernetes for use when creating or updating a cluster. The string contains both the upstream version of Kubernetes as well as the DigitalOcean revision. | String getSlug() | setSlug(String slug) |
| `SupportedFeatures` | `List<String>` | Optional | The features available with the version of Kubernetes provided by a given slug. | List<String> getSupportedFeatures() | setSupportedFeatures(List<String> supportedFeatures) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AvailableUpgradeVersion;
import java.io.IOException;
import java.util.Arrays;

AvailableUpgradeVersion availableUpgradeVersion = new AvailableUpgradeVersion.Builder()
    .kubernetesVersion("1.16.13")
    .slug("1.16.13-do.0")
    .supportedFeatures(Arrays.asList(
        "cluster-autoscaler",
        "docr-integration",
        "token-authentication"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



