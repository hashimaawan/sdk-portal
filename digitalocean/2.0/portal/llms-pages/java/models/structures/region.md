# Region

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlZ2lvbg

*This model accepts additional fields of type Object.*


# Class Name

`Region`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Available` | `boolean` | Required | This is a boolean value that represents whether new Droplets can be created in this region. | boolean getAvailable() | setAvailable(boolean available) |
| `Features` | `List<String>` | Required | This attribute is set to an array which contains features available in this region | List<String> getFeatures() | setFeatures(List<String> features) |
| `Name` | `String` | Required | The display name of the region.  This will be a full name that is used in the control panel and other interfaces. | String getName() | setName(String name) |
| `Sizes` | `List<String>` | Required | This attribute is set to an array which contains the identifying slugs for the sizes available in this region. | List<String> getSizes() | setSizes(List<String> sizes) |
| `Slug` | `String` | Required | A human-readable string that is used as a unique identifier for each region. | String getSlug() | setSlug(String slug) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Region;
import java.io.IOException;
import java.util.Arrays;

Region region = new Region.Builder(
    true,
    Arrays.asList(
        "private_networking",
        "backups",
        "ipv6",
        "metadata",
        "install_agent",
        "storage",
        "image_transfer"
    ),
    "New York 3",
    Arrays.asList(
        "s-1vcpu-1gb",
        "s-1vcpu-2gb",
        "s-1vcpu-3gb",
        "s-2vcpu-2gb",
        "s-3vcpu-1gb",
        "s-2vcpu-4gb",
        "s-4vcpu-8gb",
        "s-6vcpu-16gb",
        "s-8vcpu-32gb",
        "s-12vcpu-48gb",
        "s-16vcpu-64gb",
        "s-20vcpu-96gb",
        "s-24vcpu-128gb",
        "s-32vcpu-192g"
    ),
    "nyc3"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



