# Geographical Information about an App Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkdlb2dyYXBoaWNhbCUyNTIwaW5mb3JtYXRpb24lMjUyMGFib3V0JTI1MjBhbiUyNTIwYXBwJTI1MjBvcmlnaW4

*This model accepts additional fields of type Object.*


# Class Name

`GeographicalInformationAboutAnAppOrigin`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Continent` | `String` | Optional, Read-only | - | String getContinent() | setContinent(String continent) |
| `DataCenters` | `List<String>` | Optional, Read-only | - | List<String> getDataCenters() | setDataCenters(List<String> dataCenters) |
| `Default` | `Boolean` | Optional, Read-only | Whether or not the region is presented as the default. | Boolean getDefault() | setDefault(Boolean mDefault) |
| `Disabled` | `Boolean` | Optional, Read-only | - | Boolean getDisabled() | setDisabled(Boolean disabled) |
| `Flag` | `String` | Optional, Read-only | - | String getFlag() | setFlag(String flag) |
| `Label` | `String` | Optional, Read-only | - | String getLabel() | setLabel(String label) |
| `Reason` | `String` | Optional, Read-only | - | String getReason() | setReason(String reason) |
| `Slug` | `String` | Optional, Read-only | - | String getSlug() | setSlug(String slug) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.GeographicalInformationAboutAnAppOrigin;
import java.io.IOException;
import java.util.Arrays;

GeographicalInformationAboutAnAppOrigin geographicalInformationAboutAnAppOrigin = new GeographicalInformationAboutAnAppOrigin.Builder()
    .continent("europe")
    .dataCenters(Arrays.asList(
        "ams"
    ))
    .mDefault(true)
    .disabled(true)
    .flag("ams")
    .label("ams")
    .reason("to crowded")
    .slug("basic")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



