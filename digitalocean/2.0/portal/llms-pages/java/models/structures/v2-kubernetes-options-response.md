# V2 Kubernetes Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBPcHRpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesOptionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Options` | [`Options1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/options-1.md) | Optional | - | Options1 getOptions() | setOptions(Options1 options) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AvailableUpgradeVersion;
import com.digitalocean.api.models.Options1;
import com.digitalocean.api.models.Region4;
import com.digitalocean.api.models.Size1;
import com.digitalocean.api.models.V2KubernetesOptionsResponse;
import java.io.IOException;
import java.util.Arrays;

V2KubernetesOptionsResponse v2KubernetesOptionsResponse = new V2KubernetesOptionsResponse.Builder()
    .options(new Options1.Builder()
        .regions(Arrays.asList(
            new Region4.Builder()
                .name("name0")
                .slug("slug6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new Region4.Builder()
                .name("name0")
                .slug("slug6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
        .sizes(Arrays.asList(
            new Size1.Builder()
                .name("name0")
                .slug("slug6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new Size1.Builder()
                .name("name0")
                .slug("slug6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new Size1.Builder()
                .name("name0")
                .slug("slug6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
        .versions(Arrays.asList(
            new AvailableUpgradeVersion.Builder()
                .kubernetesVersion("kubernetes_version6")
                .slug("slug4")
                .supportedFeatures(Arrays.asList(
                    "supported_features7",
                    "supported_features8"
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new AvailableUpgradeVersion.Builder()
                .kubernetesVersion("kubernetes_version6")
                .slug("slug4")
                .supportedFeatures(Arrays.asList(
                    "supported_features7",
                    "supported_features8"
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



