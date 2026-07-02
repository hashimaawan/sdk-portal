# V2 Firewalls Tags Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFRhZ3MlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2FirewallsTagsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Tags` | `List<String>` | Required | - | List<String> getTags() | setTags(List<String> tags) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2FirewallsTagsRequest;
import java.io.IOException;
import java.util.Arrays;

V2FirewallsTagsRequest v2FirewallsTagsRequest = new V2FirewallsTagsRequest.Builder(
    Arrays.asList(
        "tags1"
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



