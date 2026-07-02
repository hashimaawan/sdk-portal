# V2 Kubernetes Clusters Clusterlint Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersClusterlintRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExcludeChecks` | `List<String>` | Optional | An array of checks that will be run when clusterlint executes checks. | List<String> getExcludeChecks() | setExcludeChecks(List<String> excludeChecks) |
| `ExcludeGroups` | `List<String>` | Optional | An array of check groups that will be omitted when clusterlint executes checks. | List<String> getExcludeGroups() | setExcludeGroups(List<String> excludeGroups) |
| `IncludeChecks` | `List<String>` | Optional | An array of checks that will be run when clusterlint executes checks. | List<String> getIncludeChecks() | setIncludeChecks(List<String> includeChecks) |
| `IncludeGroups` | `List<String>` | Optional | An array of check groups that will be run when clusterlint executes checks. | List<String> getIncludeGroups() | setIncludeGroups(List<String> includeGroups) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2KubernetesClustersClusterlintRequest;
import java.io.IOException;
import java.util.Arrays;

V2KubernetesClustersClusterlintRequest v2KubernetesClustersClusterlintRequest = new V2KubernetesClustersClusterlintRequest.Builder()
    .excludeChecks(Arrays.asList(
        "default-namespace"
    ))
    .excludeGroups(Arrays.asList(
        "workload-health"
    ))
    .includeChecks(Arrays.asList(
        "bare-pods",
        "resource-requirements"
    ))
    .includeGroups(Arrays.asList(
        "basic",
        "doks",
        "security"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



