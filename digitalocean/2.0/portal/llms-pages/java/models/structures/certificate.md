# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl

*This model accepts additional fields of type Object.*


# Class Name

`Certificate`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the certificate was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `DnsNames` | `List<String>` | Optional | An array of fully qualified domain names (FQDNs) for which the certificate was issued. | List<String> getDnsNames() | setDnsNames(List<String> dnsNames) |
| `Id` | `UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a certificate. | UUID getId() | setId(UUID id) |
| `Name` | `String` | Optional | A unique human-readable name referring to a certificate. | String getName() | setName(String name) |
| `NotAfter` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents the certificate's expiration date. | LocalDateTime getNotAfter() | setNotAfter(LocalDateTime notAfter) |
| `Sha1Fingerprint` | `String` | Optional, Read-only | A unique identifier generated from the SHA-1 fingerprint of the certificate. | String getSha1Fingerprint() | setSha1Fingerprint(String sha1Fingerprint) |
| `State` | [`State`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/state.md) | Optional, Read-only | A string representing the current state of the certificate. It may be `pending`, `verified`, or `error`. | State getState() | setState(State state) |
| `Type` | [`Type4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-4.md) | Optional | A string representing the type of the certificate. The value will be `custom` for a user-uploaded certificate or `lets_encrypt` for one automatically generated with Let's Encrypt. | Type4 getType() | setType(Type4 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Certificate;
import com.digitalocean.api.models.State;
import com.digitalocean.api.models.Type4;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

Certificate certificate = new Certificate.Builder()
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2017-02-08T16:02:37Z"))
    .dnsNames(Arrays.asList(
        "www.example.com",
        "example.com"
    ))
    .id(UUID.fromString("892071a0-bb95-49bc-8021-3afd67a210bf"))
    .name("web-cert-01")
    .notAfter(DateTimeHelper.fromRfc8601DateTime("2017-02-22T00:23:00Z"))
    .sha1Fingerprint("dfcc9f57d86bf58e321c2c6c31c7a971be244ac7")
    .state(State.VERIFIED)
    .type(Type4.LETS_ENCRYPT)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



