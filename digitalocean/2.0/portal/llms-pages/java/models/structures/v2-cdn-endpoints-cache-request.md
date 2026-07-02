# V2 Cdn Endpoints Cache Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwQ2FjaGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2CdnEndpointsCacheRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Files` | `List<String>` | Required | An array of strings containing the path to the content to be purged from the CDN cache. | List<String> getFiles() | setFiles(List<String> files) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2CdnEndpointsCacheRequest;
import java.io.IOException;
import java.util.Arrays;

V2CdnEndpointsCacheRequest v2CdnEndpointsCacheRequest = new V2CdnEndpointsCacheRequest.Builder(
    Arrays.asList(
        "path/to/image.png",
        "path/to/css/*"
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



