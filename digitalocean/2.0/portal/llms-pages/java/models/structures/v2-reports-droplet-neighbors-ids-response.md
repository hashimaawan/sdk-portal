# V2 Reports Droplet Neighbors Ids Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBSZXBvcnRzJTI1MjBEcm9wbGV0JTI1MjBOZWlnaGJvcnMlMjUyMElkcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2ReportsDropletNeighborsIdsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NeighborIds` | `List<List<Integer>>` | Optional | An array of arrays. Each array will contain a set of Droplet IDs for Droplets that share a physical server. | List<List<Integer>> getNeighborIds() | setNeighborIds(List<List<Integer>> neighborIds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2ReportsDropletNeighborsIdsResponse;
import java.io.IOException;
import java.util.Arrays;

V2ReportsDropletNeighborsIdsResponse v2ReportsDropletNeighborsIdsResponse = new V2ReportsDropletNeighborsIdsResponse.Builder()
    .neighborIds(Arrays.asList(
        Arrays.asList(
            168671828,
            168663509,
            168671815
        ),
        Arrays.asList(
            168671883,
            168671750
        )
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



