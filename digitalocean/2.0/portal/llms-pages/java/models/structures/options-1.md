# Options 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk9wdGlvbnMx

*This model accepts additional fields of type Object.*


# Class Name

`Options1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Regions` | [`List<Region4>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/region-4.md) | Optional | - | List<Region4> getRegions() | setRegions(List<Region4> regions) |
| `Sizes` | [`List<Size1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/size-1.md) | Optional | - | List<Size1> getSizes() | setSizes(List<Size1> sizes) |
| `Versions` | [`List<AvailableUpgradeVersion>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/available-upgrade-version.md) | Optional | - | List<AvailableUpgradeVersion> getVersions() | setVersions(List<AvailableUpgradeVersion> versions) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AvailableUpgradeVersion;
import com.digitalocean.api.models.Options1;
import com.digitalocean.api.models.Region4;
import com.digitalocean.api.models.Size1;
import java.io.IOException;
import java.util.Arrays;

Options1 options1 = new Options1.Builder()
    .regions(Arrays.asList(
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
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



