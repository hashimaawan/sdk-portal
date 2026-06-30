# Status 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlN0YXR1czI

Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates


# Class Name

`Status2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | [`Error2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/error-2.md) | Optional | If issuance or renewal reports `failed`, this property contains information about what happened | Error2 getError() | setError(Error2 error) |
| `Issuance` | [`IssuanceEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/issuance.md) | Optional | Status of the issuance process of the Certificate | IssuanceEnum getIssuance() | setIssuance(IssuanceEnum issuance) |
| `Renewal` | [`RenewalEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/renewal.md) | Optional | Status of the renewal process of the Certificate. | RenewalEnum getRenewal() | setRenewal(RenewalEnum renewal) |


# Example

```java
import cloud.hetzner.api.models.IssuanceEnum;
import cloud.hetzner.api.models.RenewalEnum;
import cloud.hetzner.api.models.Status2;

Status2 status2 = new Status2.Builder()
    .error(null)
    .issuance(IssuanceEnum.COMPLETED)
    .renewal(RenewalEnum.SCHEDULED)
    .build();
```



