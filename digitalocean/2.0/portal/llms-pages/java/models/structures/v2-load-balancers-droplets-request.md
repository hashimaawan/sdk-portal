# V2 Load Balancers Droplets Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMERyb3BsZXRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2LoadBalancersDropletsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DropletIds` | `List<Integer>` | Optional | An array containing the IDs of the Droplets assigned to the load balancer. | List<Integer> getDropletIds() | setDropletIds(List<Integer> dropletIds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2LoadBalancersDropletsRequest;
import java.io.IOException;
import java.util.Arrays;

V2LoadBalancersDropletsRequest v2LoadBalancersDropletsRequest = new V2LoadBalancersDropletsRequest.Builder()
    .dropletIds(Arrays.asList(
        3164444,
        3164445
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



