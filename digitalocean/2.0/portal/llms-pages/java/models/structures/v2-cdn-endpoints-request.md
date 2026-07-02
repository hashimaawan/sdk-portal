# V2 Cdn Endpoints Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2CdnEndpointsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CertificateId` | `UUID` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. | UUID getCertificateId() | setCertificateId(UUID certificateId) |
| `CustomDomain` | `String` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. | String getCustomDomain() | setCustomDomain(String customDomain) |
| `Ttl` | [`Ttl`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `Ttl.ENUM_3600` | Ttl getTtl() | setTtl(Ttl ttl) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Ttl;
import com.digitalocean.api.models.V2CdnEndpointsRequest;
import java.io.IOException;
import java.util.UUID;

V2CdnEndpointsRequest v2CdnEndpointsRequest = new V2CdnEndpointsRequest.Builder()
    .certificateId(UUID.fromString("892071a0-bb95-49bc-8021-3afd67a210bf"))
    .customDomain("static.example.com")
    .ttl(Ttl.ENUM_3600)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



