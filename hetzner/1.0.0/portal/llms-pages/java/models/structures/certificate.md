# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl


# Class Name

`Certificate`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Certificate` | `String` | Required | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding | String getCertificate() | setCertificate(String certificate) |
| `Created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) | String getCreated() | setCreated(String created) |
| `DomainNames` | `List<String>` | Required | Domains and subdomains covered by the Certificate | List<String> getDomainNames() | setDomainNames(List<String> domainNames) |
| `Fingerprint` | `String` | Required | SHA256 fingerprint of the Certificate | String getFingerprint() | setFingerprint(String fingerprint) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Labels` | `Map<String, String>` | Required | User-defined labels (key-value pairs) | Map<String, String> getLabels() | setLabels(Map<String, String> labels) |
| `Name` | `String` | Required | Name of the Resource. Must be unique per Project. | String getName() | setName(String name) |
| `NotValidAfter` | `String` | Required | Point in time when the Certificate stops being valid (in ISO-8601 format) | String getNotValidAfter() | setNotValidAfter(String notValidAfter) |
| `NotValidBefore` | `String` | Required | Point in time when the Certificate becomes valid (in ISO-8601 format) | String getNotValidBefore() | setNotValidBefore(String notValidBefore) |
| `Status` | [`Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/status-2.md) | Optional | Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates | Status2 getStatus() | setStatus(Status2 status) |
| `Type` | [`TypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type.md) | Optional | Type of the Certificate | TypeEnum getType() | setType(TypeEnum type) |
| `UsedBy` | [`List<UsedBy>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/used-by.md) | Required | Resources currently using the Certificate | List<UsedBy> getUsedBy() | setUsedBy(List<UsedBy> usedBy) |


# Example

```java
import cloud.hetzner.api.models.Certificate;
import cloud.hetzner.api.models.IssuanceEnum;
import cloud.hetzner.api.models.RenewalEnum;
import cloud.hetzner.api.models.Status2;
import cloud.hetzner.api.models.TypeEnum;
import cloud.hetzner.api.models.UsedBy;
import java.util.Arrays;
import java.util.LinkedHashMap;

Certificate certificate = new Certificate.Builder(
    "-----BEGIN CERTIFICATE-----\n...",
    "2016-01-30T23:55:00+00:00",
    Arrays.asList(
        "example.com",
        "webmail.example.com",
        "www.example.com"
    ),
    "03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f",
    42,
    new LinkedHashMap<String, String>() {{
        put("key0", "labels8");
        put("key1", "labels7");
        put("key2", "labels6");
    }},
    "my-resource",
    "2019-07-08T09:59:59+00:00",
    "2019-01-08T10:00:00+00:00",
    Arrays.asList(
        new UsedBy.Builder(
            4711,
            "load_balancer"
        )
        .build()
    )
)
.status(new Status2.Builder()
        .error(null)
        .issuance(IssuanceEnum.COMPLETED)
        .renewal(RenewalEnum.FAILED)
        .build())
.type(TypeEnum.UPLOADED)
.build();
```



