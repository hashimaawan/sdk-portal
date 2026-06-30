# Status 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXR1czI

Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates


# Class Name

`Status2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`Error2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/error-2.md) | Optional | If issuance or renewal reports `failed`, this property contains information about what happened |
| `Issuance` | [`IssuanceEnum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/issuance.md) | Optional | Status of the issuance process of the Certificate |
| `Renewal` | [`RenewalEnum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/renewal.md) | Optional | Status of the renewal process of the Certificate. |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Status2 status2 = new Status2
{
    Error = null,
    Issuance = IssuanceEnum.Completed,
    Renewal = RenewalEnum.Scheduled,
};
```



