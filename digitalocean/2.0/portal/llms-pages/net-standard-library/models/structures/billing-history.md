# Billing History

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkJpbGxpbmdIaXN0b3J5

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`BillingHistory`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Amount` | `string` | Optional | Amount of the billing history entry. |
| `Date` | `DateTime?` | Optional | Time the billing history entry occurred. |
| `Description` | `string` | Optional | Description of the billing history entry. |
| `InvoiceId` | `string` | Optional | ID of the invoice associated with the billing history entry, if  applicable. |
| `InvoiceUuid` | `string` | Optional | UUID of the invoice associated with the billing history entry, if  applicable. |
| `Type` | [`Type6?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/type-6.md) | Optional | Type of billing history entry. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

BillingHistory billingHistory = new BillingHistory
{
    Amount = "12.34",
    Date = DateTime.ParseExact("2018-06-01T08:44:38Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Description = "Invoice for May 2018",
    InvoiceId = "123",
    InvoiceUuid = "example-uuid",
    Type = Type6.Invoice,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



