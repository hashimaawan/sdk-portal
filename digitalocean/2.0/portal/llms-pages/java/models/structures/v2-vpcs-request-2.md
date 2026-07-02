# V2 Vpcs Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBWcGNzJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type Object.*


# Class Name

`V2VpcsRequest2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | A free-form text field for describing the VPC's purpose. It may be a maximum of 255 characters.<br><br>**Constraints**: *Maximum Length*: `255` | String getDescription() | setDescription(String description) |
| `Name` | `String` | Required | The name of the VPC. Must be unique and may only contain alphanumeric characters, dashes, and periods.<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9\-\.]+$` | String getName() | setName(String name) |
| `Default` | `Boolean` | Optional | A boolean value indicating whether or not the VPC is the default network for the region. All applicable resources are placed into the default VPC network unless otherwise specified during their creation. The `default` field cannot be unset from `true`. If you want to set a new default VPC network, update the `default` field of another VPC network in the same region. The previous network's `default` field will be set to `false` when a new default VPC has been defined. | Boolean getDefault() | setDefault(Boolean mDefault) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2VpcsRequest2;
import java.io.IOException;

V2VpcsRequest2 v2VpcsRequest2 = new V2VpcsRequest2.Builder(
    "env.prod-vpc"
)
.description("VPC for production environment")
.mDefault(true)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



