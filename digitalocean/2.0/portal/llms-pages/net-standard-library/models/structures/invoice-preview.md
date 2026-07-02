# Invoice Preview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkludm9pY2VQcmV2aWV3

The invoice preview.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`InvoicePreview`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Amount` | `string` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. |
| `InvoicePeriod` | `string` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. |
| `InvoiceUuid` | `string` | Optional | The UUID of the invoice. The canonical reference for the invoice. |
| `UpdatedAt` | `string` | Optional | Time the invoice was last updated.  This is only included with the invoice preview. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

InvoicePreview invoicePreview = new InvoicePreview
{
    Amount = "23.45",
    InvoicePeriod = "2020-01",
    InvoiceUuid = "fdabb512-6faf-443c-ba2e-665452332a9e",
    UpdatedAt = "2020-01-23T06:31:50Z",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



