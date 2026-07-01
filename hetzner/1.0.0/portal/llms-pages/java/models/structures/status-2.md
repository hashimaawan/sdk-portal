# Status 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXR1czI

Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates

*This model accepts additional fields of type Object.*


# Class Name

`Status2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | [`Error2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/error-2.md) | Optional | If issuance or renewal reports `failed`, this property contains information about what happened | Error2 getError() | setError(Error2 error) |
| `Issuance` | [`Issuance`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/issuance.md) | Optional | Status of the issuance process of the Certificate | Issuance getIssuance() | setIssuance(Issuance issuance) |
| `Renewal` | [`Renewal`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/renewal.md) | Optional | Status of the renewal process of the Certificate. | Renewal getRenewal() | setRenewal(Renewal renewal) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Issuance;
import cloud.hetzner.api.models.Renewal;
import cloud.hetzner.api.models.Status2;
import java.io.IOException;

Status2 status2 = new Status2.Builder()
    .error(null)
    .issuance(Issuance.COMPLETED)
    .renewal(Renewal.SCHEDULED)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



