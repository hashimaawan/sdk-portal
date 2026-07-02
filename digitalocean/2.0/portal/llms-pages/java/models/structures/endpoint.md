# Endpoint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkVuZHBvaW50

*This model accepts additional fields of type Object.*


# Class Name

`Endpoint`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CertificateId` | `UUID` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. | UUID getCertificateId() | setCertificateId(UUID certificateId) |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the CDN endpoint was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `CustomDomain` | `String` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. | String getCustomDomain() | setCustomDomain(String customDomain) |
| `Endpoint` | `String` | Optional, Read-only | The fully qualified domain name (FQDN) from which the CDN-backed content is served. | String getEndpoint() | setEndpoint(String endpoint) |
| `Id` | `UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a CDN endpoint. | UUID getId() | setId(UUID id) |
| `Origin` | `String` | Required | The fully qualified domain name (FQDN) for the origin server which provides the content for the CDN. This is currently restricted to a Space. | String getOrigin() | setOrigin(String origin) |
| `Ttl` | [`Ttl`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `Ttl.ENUM_3600` | Ttl getTtl() | setTtl(Ttl ttl) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Endpoint;
import com.digitalocean.api.models.Ttl;
import java.io.IOException;
import java.util.UUID;

Endpoint endpoint = new Endpoint.Builder(
    "static-images.nyc3.digitaloceanspaces.com"
)
.certificateId(UUID.fromString("892071a0-bb95-49bc-8021-3afd67a210bf"))
.createdAt(DateTimeHelper.fromRfc8601DateTime("2018-03-21T16:02:37Z"))
.customDomain("static.example.com")
.endpoint("static-images.nyc3.cdn.digitaloceanspaces.com")
.id(UUID.fromString("892071a0-bb95-49bc-8021-3afd67a210bf"))
.ttl(Ttl.ENUM_3600)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



