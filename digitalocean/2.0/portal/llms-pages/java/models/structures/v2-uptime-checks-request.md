# V2 Uptime Checks Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2UptimeChecksRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Enabled` | `Boolean` | Optional | A boolean value indicating whether the check is enabled/disabled.<br><br>**Default**: `true` | Boolean getEnabled() | setEnabled(Boolean enabled) |
| `Name` | `String` | Optional | A human-friendly display name. | String getName() | setName(String name) |
| `Regions` | [`List<Region8>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/region-8.md) | Optional | An array containing the selected regions to perform healthchecks from. | List<Region8> getRegions() | setRegions(List<Region8> regions) |
| `Target` | `String` | Optional | The endpoint to perform healthchecks on. | String getTarget() | setTarget(String target) |
| `Type` | [`Type19`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-19.md) | Optional | The type of health check to perform. | Type19 getType() | setType(Type19 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Region8;
import com.digitalocean.api.models.Type19;
import com.digitalocean.api.models.V2UptimeChecksRequest;
import java.io.IOException;
import java.util.Arrays;

V2UptimeChecksRequest v2UptimeChecksRequest = new V2UptimeChecksRequest.Builder()
    .enabled(true)
    .name("Landing page check")
    .regions(Arrays.asList(
        Region8.US_EAST,
        Region8.EU_WEST
    ))
    .target("https://www.landingpage.com")
    .type(Type19.HTTPS)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



