# V2 Apps Regions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZWdpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsRegionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Regions` | [`List<GeographicalInformationAboutAnAppOrigin>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/geographical-information-about-an-app-origin.md) | Optional | - | List<GeographicalInformationAboutAnAppOrigin> getRegions() | setRegions(List<GeographicalInformationAboutAnAppOrigin> regions) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.GeographicalInformationAboutAnAppOrigin;
import com.digitalocean.api.models.V2AppsRegionsResponse;
import java.io.IOException;
import java.util.Arrays;

V2AppsRegionsResponse v2AppsRegionsResponse = new V2AppsRegionsResponse.Builder()
    .regions(Arrays.asList(
        new GeographicalInformationAboutAnAppOrigin.Builder()
            .continent("continent2")
            .dataCenters(Arrays.asList(
                "data_centers9"
            ))
            .mDefault(false)
            .disabled(false)
            .flag("flag4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



