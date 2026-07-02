# Let S Encrypt Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxldCUyNTI3cyUyNTIwRW5jcnlwdCUyNTIwQ2VydGlmaWNhdGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`LetSEncryptCertificateRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | A unique human-readable name referring to a certificate. | String getName() | setName(String name) |
| `Type` | [`Type4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-4.md) | Optional | A string representing the type of the certificate. The value will be `custom` for a user-uploaded certificate or `lets_encrypt` for one automatically generated with Let's Encrypt. | Type4 getType() | setType(Type4 type) |
| `DnsNames` | `List<String>` | Required | An array of fully qualified domain names (FQDNs) for which the certificate was issued. A certificate covering all subdomains can be issued using a wildcard (e.g. `*.example.com`). | List<String> getDnsNames() | setDnsNames(List<String> dnsNames) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.LetSEncryptCertificateRequest;
import com.digitalocean.api.models.Type4;
import java.io.IOException;
import java.util.Arrays;

LetSEncryptCertificateRequest letSEncryptCertificateRequest = new LetSEncryptCertificateRequest.Builder(
    "web-cert-01",
    Arrays.asList(
        "www.example.com",
        "example.com"
    )
)
.type(Type4.LETS_ENCRYPT)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



