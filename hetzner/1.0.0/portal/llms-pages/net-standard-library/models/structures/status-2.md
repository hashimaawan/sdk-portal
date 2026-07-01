# Status 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXR1czI

Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates

*This model accepts additional fields of type object.*


# Class Name

`Status2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`Error2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/error-2.md) | Optional | If issuance or renewal reports `failed`, this property contains information about what happened |
| `Issuance` | [`Issuance?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/issuance.md) | Optional | Status of the issuance process of the Certificate |
| `Renewal` | [`Renewal?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/renewal.md) | Optional | Status of the renewal process of the Certificate. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

Status2 status2 = new Status2
{
    Error = null,
    Issuance = Issuance.Completed,
    Renewal = Renewal.Scheduled,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



