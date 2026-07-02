# V2 Customers My Invoices Summary Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwU3VtbWFyeSUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2CustomersMyInvoicesSummaryResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Amount` | `string` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. |
| `BillingPeriod` | `string` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. |
| `CreditsAndAdjustments` | [`CreditsAndAdjustments`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/credits-and-adjustments.md) | Optional | - |
| `InvoiceUuid` | `string` | Optional | UUID of the invoice |
| `Overages` | [`Overages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/overages.md) | Optional | - |
| `ProductCharges` | [`ProductCharges`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/product-charges.md) | Optional | - |
| `Taxes` | [`Taxes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/taxes.md) | Optional | - |
| `UserBillingAddress` | [`UserBillingAddress`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/user-billing-address.md) | Optional | - |
| `UserCompany` | `string` | Optional | Company of the DigitalOcean customer being invoiced, if set. |
| `UserEmail` | `string` | Optional | Email of the DigitalOcean customer being invoiced. |
| `UserName` | `string` | Optional | Name of the DigitalOcean customer being invoiced. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

V2CustomersMyInvoicesSummaryResponse v2CustomersMyInvoicesSummaryResponse = new V2CustomersMyInvoicesSummaryResponse
{
    Amount = "27.13",
    BillingPeriod = "2020-01",
    CreditsAndAdjustments = new CreditsAndAdjustments
    {
        Amount = "amount6",
        Name = "name4",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    InvoiceUuid = "22737513-0ea7-4206-8ceb-98a575af7681",
    Overages = new Overages
    {
        Amount = "amount6",
        Name = "name4",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    UserCompany = "DigitalOcean",
    UserEmail = "sammy@digitalocean.com",
    UserName = "Sammy Shark",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



