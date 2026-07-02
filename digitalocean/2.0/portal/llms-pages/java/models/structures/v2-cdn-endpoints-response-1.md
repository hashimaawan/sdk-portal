# V2 Cdn Endpoints Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`V2CdnEndpointsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Endpoint` | [`Endpoint`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/endpoint.md) | Optional | - | Endpoint getEndpoint() | setEndpoint(Endpoint endpoint) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Endpoint;
import com.digitalocean.api.models.V2CdnEndpointsResponse1;
import java.io.IOException;
import java.util.UUID;

V2CdnEndpointsResponse1 v2CdnEndpointsResponse1 = new V2CdnEndpointsResponse1.Builder()
    .endpoint(new Endpoint.Builder(
        "origin2"
    )
    .certificateId(UUID.fromString("00001b94-0000-0000-0000-000000000000"))
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .customDomain("custom_domain6")
    .endpoint("endpoint6")
    .id(UUID.fromString("00001f7a-0000-0000-0000-000000000000"))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



