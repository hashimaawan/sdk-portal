# V2 1 Clicks Kubernetes Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjAxJTI1MjBDbGlja3MlMjUyMEt1YmVybmV0ZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V21ClicksKubernetesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AddonSlugs` | `List<String>` | Required | An array of 1-Click Application slugs to be installed to the Kubernetes cluster. | List<String> getAddonSlugs() | setAddonSlugs(List<String> addonSlugs) |
| `ClusterUuid` | `String` | Required | A unique ID for the Kubernetes cluster to which the 1-Click Applications will be installed. | String getClusterUuid() | setClusterUuid(String clusterUuid) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V21ClicksKubernetesRequest;
import java.io.IOException;
import java.util.Arrays;

V21ClicksKubernetesRequest v21ClicksKubernetesRequest = new V21ClicksKubernetesRequest.Builder(
    Arrays.asList(
        "kube-state-metrics",
        "loki"
    ),
    "50a994b6-c303-438f-9495-7e896cfe6b08"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



