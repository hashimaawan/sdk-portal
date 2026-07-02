# V2 Firewalls Droplets Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMERyb3BsZXRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2FirewallsDropletsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DropletIds` | `List<Integer>` | Required | An array containing the IDs of the Droplets to be removed from the firewall. | List<Integer> getDropletIds() | setDropletIds(List<Integer> dropletIds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2FirewallsDropletsRequest;
import java.io.IOException;
import java.util.Arrays;

V2FirewallsDropletsRequest v2FirewallsDropletsRequest = new V2FirewallsDropletsRequest.Builder(
    Arrays.asList(
        49696269
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



